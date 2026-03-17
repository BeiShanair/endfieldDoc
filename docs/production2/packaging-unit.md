---
sidebar_position: 3
---

# 封装机 / Packaging Unit

用于封装部分能量元件的设备

A facility for packaging certain power components

## 画廊 / Gallery
![Packaging Unit](img/17.jpg)

## 信息 / Information
- 封装机`需要电力`才能工作，耗电量为`20 EFU`；

  Packaging Unit needs power to work, power consumption is `20 EFU`;

- 每`10秒`加工一个物品，相关配方见`JEI`或`REI`；

  Each `10 seconds` process one item, related recipes see `JEI` or `REI`;

## Tips
- 可通过`制造台`制作，相关介绍见[制作台](../production1/crafter.md)；

  It can be made through the Crafter, see [Crafter](../production1/crafter.md) for details;

- 放置`封装机`需要`6×4`的空地

  Placing a Packaging Unit requires an empty `6×4` area

## 相关配方 / Related Recipes
你可自定义数据包来拓展封装机能加工的东西；

You can customize the data pack to expand the things that the Packaging Unit can process;

### 示例 / Example：
```json
{
  "type": "arknights_endfield:packaging_unit",
  "input": [
    {
      "count": 10,
      "item": "arknights_endfield:steel_part"
    },
    {
      "count": 20,
      "item": "arknights_endfield:dense_originium_powder"
    }
  ],
  "output": {
    "count": 1,
    "item": "arknights_endfield:hc_battery"
  }
}
```

参数说明 / Parameter Description:
- `input`: 输入物品和数量 / Input items and number;
- `output`: 合成物品和数量 / Output items and number;