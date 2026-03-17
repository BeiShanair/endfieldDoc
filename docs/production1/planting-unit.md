---
sidebar_position: 6
---

# 种植机 / Planting Unit

能够培育各类普通植物的仓形设备

A cultivating silo for growing various common plants and crops

## 画廊 / Gallery
![Planting Unit](img/13.jpg)

## 信息 / Information
- 种植机`需要电力`才能工作，耗电量为`20 EFU`；

  Planting Unit needs power to work, power consumption is `20 EFU`;

- 每`2秒`加工一个物品，相关配方见`JEI`或`REI`；

  Each `2 seconds` process one item, related recipes see `JEI` or `REI`;

## Tips
- 可通过`制造台`制作，相关介绍见[制作台](crafter.md)；

  It can be made through the Crafter, see [Crafter](crafter.md) for details;

- 放置`种植机`需要`5×5`的空地

  Placing a Planting Unit requires an empty `5×5` area

## 相关配方 / Related Recipes
你可自定义数据包来拓展种植机能加工的东西；

You can customize the data pack to expand the things that the Planting Unit can process;

### 示例 / Example：
```json
{
  "type": "arknights_endfield:planting_unit",
  "input": {
    "item": "arknights_endfield:buckflower_seed"
  },
  "output": {
    "count": 1,
    "item": "arknights_endfield:buckflower"
  }
}
```

参数说明 / Parameter Description:
- `input`: 输入物品 / Input items;
- `output`: 合成物品和数量 / Output items and number;