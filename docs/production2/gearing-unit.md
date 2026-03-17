---
sidebar_position: 1
---

# 装备原件机 / Gearing Unit

能够将不同材料嵌合加工成装备原件的设备

A facility that laminates different materials together to create gear components

## 画廊 / Gallery
![Gearing Unit](img/16.jpg)

## 信息 / Information
- 装备原件机`需要电力`才能工作，耗电量为`10 EFU`；

  Gearing Unit needs power to work, power consumption is `10 EFU`;

- 每`10秒`加工一个物品，相关配方见`JEI`或`REI`；

  Each `10 seconds` process one item, related recipes see `JEI` or `REI`;

## Tips
- 可通过`制造台`制作，相关介绍见[制作台](../production1/crafter.md)；

  It can be made through the Crafter, see [Crafter](../production1/crafter.md) for details;

- 放置`装备原件机`需要`6×4`的空地

  Placing a Gearing Unit requires an empty `6×4` area

## 相关配方 / Related Recipes
你可自定义数据包来拓展装备原件机能加工的东西；

You can customize the data pack to expand the things that the Gearing Unit can process;

### 示例 / Example：
```json
{
  "type": "arknights_endfield:gearing_unit",
  "input": [
    {
      "count": 5,
      "item": "arknights_endfield:origocrust"
    },
    {
      "count": 5,
      "item": "arknights_endfield:amethyst_fiber"
    }
  ],
  "output": {
    "count": 1,
    "item": "arknights_endfield:amethyst_component"
  }
}
```

参数说明 / Parameter Description:
- `input`: 输入物品和数量 / Input items and number;
- `output`: 合成物品和数量 / Output items and number;