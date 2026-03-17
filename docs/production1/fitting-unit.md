---
sidebar_position: 4
---

# 配件机 / Fitting Unit

能够加工各式零件的平台

A facility capable of processing various parts

## 画廊 / Gallery
![Fitting Unit](img/10.jpg)
*尚未修改的模型版本，参考再次测试*

## 信息 / Information
- 配件机`需要电力`才能工作，耗电量为`20 EFU`；

  Fitting Unit needs power to work, power consumption is `20 EFU`;

- 每`2秒`加工一个物品，相关配方见`JEI`或`REI`；

  Each `2 seconds` process one item, related recipes see `JEI` or `REI`;

## Tips
- 可通过`制造台`制作，相关介绍见[制作台](crafter.md)；

  It can be made through the Crafter, see [Crafter](crafter.md) for details;

- 放置`配件机`需要`3×3`的空地

  Placing a Fitting Unit requires an empty `3×3` area

## 相关配方 / Related Recipes
你可自定义数据包来拓展配件机能加工的东西；

You can customize the data pack to expand the things that the Fitting Unit can process;

### 示例 / Example：
```json
{
  "type": "arknights_endfield:fitting_unit",
  "input": {
    "item": "arknights_endfield:amethyst_fiber"
  },
  "output": {
    "count": 1,
    "item": "arknights_endfield:amethyst_part"
  }
}
```

参数说明 / Parameter Description:
- `input`: 输入物品 / Input items;
- `output`: 合成物品和数量 / Output items and number;