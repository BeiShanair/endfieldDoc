---
sidebar_position: 3
---

# 全局电网节点管理系统 / Global Power Network Node Manager

单例模式，负责处理协议核心、供电桩、中继器以及用电工业设备与它们之间的连接

Singleton mode, responsible for handling Protocol Core, Electric Pylon, Relay Tower and the connection between power industry devices and them

## 信息 / Information
- 该系统在一个世界上只存在一个实例，不过不用依靠`tick`运行，本身只维护一个`Map`

  This system only exists one instance in a world, but not rely on `tick` to run, it only maintains a `Map`

- `协议核心`、`供电桩`、`中继器`以及所有`用电工业设备`与它有直接联系，处理它们之间的连接关系

  `Protocol Core`、`Electric Pylon`、`Relay Tower` and all `Electric Industrial Device` are connected to it directly, handle the connection between them

- 上述方块在放置时，除了用电工业设备，其他会自动向管理器注册，`供电桩`、`中继器`在放置时还会选择`Map`中最近的节点进行连接

  The above blocks are automatically registered when they are placed, except for `Electric Industrial Device`, other blocks will automatically register themselves, `Electric Pylon` and `Relay Tower` will also select the nearest node in `Map` to connect when placed

## 技术性说明 / Technical Explanation
这个单例的出现是为了解决`协议核心`、`供电桩`、`中继器`，以及`用电工业设备`与`供电桩`和`中继器`之间的连接问题；

曾经它们之间的连接只靠`遍历`，但遍历的效率非常低，而且极其耗费性能；

于是，从`全局电网管理系统`衍生出来了`全局电网节点管理系统`；

依赖这个系统，`协议核心`、`供电桩`、`中继器`以及所有`用电工业设备`不再需要靠`遍历`来寻找最近的`节点`，极大地降低了性能消耗；

`用电工业设备`则会在各自的`tick`逻辑中，每隔`1秒`检查与最近节点（`供电桩`、`中继器`）的距离，如果在`10`米范围内，则可以正常工作，否则将无法工作；

`供电桩`、`中继器`在放置时将会从`全局节点列表`中寻找最接近的`节点`，并尝试连接，节点间最大距离为`80`米；

This single instance is designed to solve the connection problem between `Protocol Core`、`Electric Pylon`、`Relay Tower`, and all `Electric Industrial Device` and `Electric Pylon` and `Relay Tower`;

In the past, they were connected only through `traversal`, which is very slow and very expensive in terms of performance;

So, from `Global Power Network Management System`, `Global Power Network Node Management System` was born;

Dependency on this system, `Protocol Core`、`Electric Pylon`、`Relay Tower`, and all `Electric Industrial Device` no longer need to rely on `traversal` to find the nearest `node`, which greatly reduces the performance consumption;

When placing `Electric Pylon`、`Relay Tower`, it will try to connect to the nearest `node` from the `global node list`, and the maximum distance between nodes is `80` meters;

`Electric Industrial Device` will check the distance between the nearest node (`Electric Pylon`、`Relay Tower`) every `1 second`, and can work normally if the distance is within `10` meters, otherwise it will not work;
