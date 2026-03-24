---
sidebar_position: 3
---
# 特性 / Features
一些已知特性，俗称bug；

Some known features, commonly known as bugs;

还有一些是区别于游戏原作的特殊设计；

Some are special designs different from the original game;

## 详细说明：
### 1. *供电桩* 或者 *中继器* 即使不接入电网，仍然可以让周围的用电工业设备正常工作
这是一个特性，将予以**保留**；

因为这与我当时想实现的`超远距电力`运输类似，也就是你把协议核心扔在你的出生点（出生点区块会保持常加载）

然后跑十万八千里去戳一个`供电桩`，仍可支持用电工业设备工作

此特性应该是因为用电工业设备与`全局电网管理系统`直接连接导致的，不过挺好的，所以也就不修了

当然，如果发电功率不够且电网本身的`电池储能`和工业设备自身的`电池储能`不足时，工业设备还是会停止工作

### 2. 用电工业设备储电、耗电相关
本模组中的所有用电工业设备，在原作基础上做了一定的特殊设计；

每个用电工业设备都会带`10000 EFU`的电池储能，以确保在电力供应不足时，避免机器直接停机；

在其电池未充满时，还是会消耗电力；而在电池充满后，且不工作的状态下，就不会消耗电力了；

电池充能速度为`该设备耗电功率的20倍`，比如耗电功率为`5 EFU/t`，则充能速度为`100 EFU/t`，不过你不需要知道剩下的`95 EFU/t`是哪来的

:::warning

`FE转换器`无此特性；

:::

模组中没有明确说明时，所用的时间单位为`tick`，而不是`秒`；在`Minecraft`中，`tick`为`1/20秒`；

所以在整个电网的用电功率大于发电功率时，电网本身的`电池储能`消耗速度会比原作快得多；

### 3. EFU
即`Endfield Units`，是本模组使用的电力单位；

因为模组的电力网络是独立存在的，即便没有其他模组仍可正常工作，所以其实它本来就没单位；

但为了能更好地区分和说明，使用了`EFU`作为本模组的电力单位；

后续的流体单位则使用通用的`B`与`mB`；

## Details (Translate with DeepL):
### 1. *Electric Pylons* or *Relay Towers* can keep nearby industrial equipment running normally even when not connected to the power grid.
This is a feature that will be **retained**;

This is similar to the `ultra-long-distance power transmission` I originally intended to implement, where you place the protocol core at your spawn point (the spawn point chunk remains constantly loaded)

and then travel a great distance to activate an `Electric Pylon`, you can still keep your power-consuming industrial equipment running.

This behavior likely stems from the fact that power-consuming industrial equipment is directly connected to the `Global Network Manager`, but since it works well, I’ve decided not to fix it.

Of course, if the power generation capacity is insufficient and both the grid’s own `battery storage` and the industrial equipment’s own `battery storage` are depleted, the industrial equipment will still stop working.

### 2. Power Storage and Consumption for Electrical Industrial Equipment
All electrical industrial equipment in this module has been specially modified from the original design;

Each piece of electrical industrial equipment comes with a battery storage capacity of `10,000 EFU` to prevent the machine from shutting down immediately when power supply is insufficient;

The device will continue to consume power while its battery is not fully charged; however, once the battery is fully charged and the device is idle, it will not consume power;

The battery charges at a rate of `20 times the device’s power consumption`. For example, if the power consumption is `5 EFU/t`, the charging rate is `100 EFU/t`—though you don’t need to know where the remaining `95 EFU/t` comes from

:::warning

Attention! The `FE Converter` does not have this feature;

:::

Unless otherwise specified in the mod, the unit of time used is `tick`, not `seconds`; in `Minecraft`, a `tick` is `1/20 of a second`;

Therefore, when the total power consumption of the grid exceeds its power generation capacity, the grid’s own `battery storage` will deplete much faster than in the original game;

### 3. EFU
Stands for `Endfield Units`, which is the unit of power used by this mod;

Since the mod’s power network exists independently and functions normally even without other mods, it does not actually have a unit by default;

However, to better distinguish and describe it, `EFU` is used as the unit of power for this mod;

Subsequent fluid units will use the standard `B` and `mB`;