---
sidebar_position: 1
---

# 传送带 / Belt

可以用来运输物品

You can use it to transport items.

## 画廊 / Gallery
![Belt](../img/example2.jpg)

## 信息 / Information
- 可以用来运输物品；

  You can use it to transport items;

- 放置逻辑参考了`Minecraft`原版的铁轨，并做了一定的拓展，可悬空放置；

  Logic placement is based on the `Minecraft` original Rail, and some extensions are made, and can be placed suspended.

- 传送带上物品的运输方向由推送端（工业设备）决定，所以在放置时无需考虑放置方向

  The direction of the transportation of items on the belt is determined by the push end (industrial device), so there is no need to consider the placement direction when placing

- 辅助铺设传送带的还有`物流桥`、`分流器`和`汇流器`，详见[传送带辅助桥](../logistics-units/logistics-bridge.md)；

  There are also `Belt bridges`, `Splitter` and `Converger` for placing belts, see [Logistics Bridge](../logistics-units/logistics-bridge.md) for details.

## Tips
并列摆放时，按住`Shift`可获得更好的效果

When arranging in parallel, hold `Shift` to get a better result

## 技术性说明 / Technical Explanation
传送带采用了`被动接受 + 主动推送`的逻辑，即：
- 推送端（工业设备）主动向与推送方向一致的传送带推送物品，并为传送带指定推送方向；
- 传送带按照推送方向进行物品的运输，并开始模拟运输（物品通过方块实体渲染器进行渲染）；
- 当推送方向上是另一个传送带时，则继续推送给下一个传送带，并为其指定推送方向，以此类推；
- 当推送方向上是另一个工业设备或是储物方块时，则将物品输入其中；

由于除了终末地相关的工业设备可以向传送带主动推送物品外，其他的，比如一些储物方块，并不能向传送带推送物品，所以新增了一个`输出端口`，详见[输出端口](../logistics-units/output-port.md)

The logic of the belt is `passive acceptance + active push`, that is:
- The industrial device pushes items to the belt in the direction consistent with the push direction, and specifies the push direction for the belt;
- The belt transports the items according to the push direction and starts to simulate the transportation (the items are rendered through the block entity renderer).
- When the push direction is another belt, it continues to push to the next belt and specifies the push direction, and so on.
- When the push direction is another industrial device or a storage block, the items are input into it.

Because only industrial devices related to the Endfield can actively push items to the belt, other things, such as some storage blocks, cannot push items to the belt, so a new `output port` is added, see [Output Port](../logistics-units/output-port.md)