---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint 接口"
linktitle: "IChartDataPoint"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint 接口。包含 C++ 中图表上单个数据点的属性。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


包含图表上单个数据点的属性。

```cpp
class IChartDataPoint : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | 指定气泡图中的气泡是否应应用 3D 效果。 |
| virtual [get_Explosion](./get_explosion/)() | 指定数据点应从饼图中心移动的距离。可以为负，负值表示未设置此属性且不应应用爆炸效果。仅适用于饼图。 |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | 指定当值为负时，父元素是否应反转其颜色。 |
| virtual [get_Marker](./get_marker/)() | 指定数据标记。请求时会自动创建标记。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | 用于 [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/) 的设置器。 |
| virtual [set_Explosion](./set_explosion/)(int32_t) | 用于 [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/) 的设置器。 |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | 指定当值为负时，父元素是否应反转其颜色。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
