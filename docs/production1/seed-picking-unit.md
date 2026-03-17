---
sidebar_position: 7
---

# 采种机 / Seed-Picking Unit

能够采集普通植物种子的设备

A facility that extracts seeds from common crops

## 画廊 / Gallery
![Seed-Picking Unit](img/12.jpg)
*尚未修改的模型版本，参考再次测试*

## 信息 / Information
- 采种机`需要电力`才能工作，耗电量为`10 EFU`；

  Seed-Picking Unit needs power to work, power consumption is `10 EFU`;

- 每`2秒`加工一个物品，相关配方见`JEI`或`REI`；

  Each `2 seconds` process one item, related recipes see `JEI` or `REI`;

## Tips
- 可通过`制造台`制作，相关介绍见[制作台](crafter.md)；

  It can be made through the Crafter, see [Crafter](crafter.md) for details;

- 放置`采种机`需要`5×5`的空地

  Placing a Seed-Picking Unit requires an empty `5×5` area

## 相关配方 / Related Recipes
你可自定义数据包来拓展采种机能加工的东西；

You can customize the data pack to expand the things that the Seed-Picking Unit can process;

### 示例 / Example：
```json
{
  "type": "arknights_endfield:seed_picking_unit",
  "input": {
    "item": "arknights_endfield:aketine"
  },
  "output": {
    "count": 2,
    "item": "arknights_endfield:aketine_seed"
  }
}
```

参数说明 / Parameter Description:
- `input`: 输入物品 / Input items;
- `output`: 合成物品和数量 / Output items and number;