---
title: "Aspose::Words::Drawing::Charts::ChartStyle enum"
linktitle: "ChartStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartStyle enum。指定 C++ 中图表的预定义样式。"
type: docs
weight: 27875
url: /zh/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


指定图表的预定义样式。

```cpp
enum class ChartStyle
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 普通 | 0 | 表示默认的图表样式。 |
| Muted | 1 | 一种使用柔和颜色的样式。 |
| Saturated | 2 | 一种使用更饱和颜色的样式。 |
| Shaded | 3 | 一种带有阴影数据点的样式。 |
| Flat | 4 | 一种平面数据点且无渐变的样式。 |
| Shadowed | 5 | 一种数据点带有阴影的样式。 |
| 渐变 | 6 | 一种数据点具有渐变填充的样式。 |
| 原始 | 7 | 一种图表具有原始外观的样式。 |
| Transparent1 | 8 | 一种数据点透明的样式。 |
| Transparent2 | 9 | 一种数据点透明的样式。 |
| Outline | 10 | 一种数据点没有填充，仅有轮廓的样式。 |
| OutlineBlack | 11 | 一种图表背景为黑色，且数据点没有填充，仅有轮廓的样式。 |
| 黑色 | 12 | 一种图表背景为黑色的样式。 |
| 灰色 | 13 | 一种图表背景为灰色渐变的样式。 |
| 蓝色 | 14 | 一种图表背景为蓝色的样式。 |
| ShadedPlot | 15 | 一种绘图区域被阴影覆盖的样式。 |


## 示例



展示如何设置和获取图表样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在黑色样式中插入图表。
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// 获取要更新的图表。
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 获取图表样式。
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
