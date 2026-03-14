---
sidebar_position: 2
---

# 全局电网管理系统 / Global Power Network Manager

单例模式，负责整个世界的电力供应

Singleton mode, responsible for the power supply of the entire world

## 信息 / Information
- 该系统在一个世界上只存在一个实例，依靠服务器的`tick`运行

  This system only exists one instance in a world, dependent on the server's `tick` to run

- `协议核心`、`供电桩`、`中继器`、`热能池`以及所有`用电工业设备`与它有直接联系，直接负责计算发电功率和用电功率

  `Protocol Core`、`Electric Pylon`、`Relay Tower`、`Thermal Bank` and all `Electric Industrial Device` are connected to it directly, directly responsible for calculating the power of generation and the power of consumption

- 上述方块在放置时，会自动向管理器注册，并按照类型参与电力计算；

  The above blocks are automatically registered when they are placed, and participate in the calculation of electricity according to type;

- 与`全局电网管理系统`相配合的，还有`全局电网节点管理系统`，详细参见[全局电网节点管理系统](../powering/global-power-network-node-manager.md)；

  There is also a `Global Power Network Node Manager` that cooperates with `Global Power Network Manager`, see [Global Power Network Node Manager](../powering/global-power-network-node-manager.md) for details.  

## Tips
强烈建议直接将`协议核心`放置在你的出生点区块附近，或者将`协议核心`所在区块设定为`常加载区块`，以保证电力系统的运行

It is strongly recommended to place the `Protocol Core` near your birth point chunk or set the chunk where the `Protocol Core` is located as a `Ticking area` to ensure the operation of the electricity system

## 技术性说明 / Technical Explanation
考虑到`Minecraft`基于`区块`运算的特性，即如果没有玩家加载方块实体所在的`区块`，那么该区块上的方块实体都会停止运算，
那么会导致协议核心电力供应相关运算终止，逻辑就跑不通了；

而强制加载区块和遍历方块实体所在的区块一定程度上会影响性能，所以现在，由`全局电网管理系统`负责整个世界的电力调度；

本质上来说，它是用来实现超远距的电力运输；

即便在单人存档，你可以直接用`中继器`将电拉到距离`协议核心`（`放在出生点区块或设定为常加载区块上`）几千格之外，也可以继续让用电工业设备正常工作；


Considered that `Minecraft` is based on the characteristics of `chunk` operation, that is, if the player does not load the `chunk` entity in the `chunk`, then all the block entities in the `chunk` will stop operating,
then the protocol core electricity supply related calculation will stop, and the logic will not be able to run.

But forcing the loading of chunks and traversing the chunks where the block entities are located somewhat affects performance, so now, the `Global Power Network Manager` is responsible for the entire world's electricity scheduling;

Essentially, it is used to implement super long distance electricity transportation;

Even in single player, you can directly use `Relay Tower` to pull the electricity to a distance of thousands of blocks away from the `Protocol Core` (placed in the birth block or set as a constant load block), and you can continue to make the electricity industry work normally;

