---
title: "Aspose::Words::Drawing::Charts::LegendPosition 枚举"
linktitle: "LegendPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::LegendPosition 枚举。指定图表图例在 C++ 中的可能位置。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


指定图例可能的位置。

```cpp
enum class LegendPosition
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 不会为图表显示图例。 |
| 底部 | 1 | 指定图例应绘制在图表的底部。 |
| 左 | 2 | 指定图例应绘制在图表的左侧。 |
| 右 | 3 | 指定图例应绘制在图表的右侧。 |
| 顶部 | 4 | 指定图例应绘制在图表的顶部。 |
| TopRight | 5 | 指定图例应绘制在图表的右上角。 |


## 示例



展示如何编辑图表图例的外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// 将图表的图例移动到右上角。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// 通过允许它们覆盖图例，为其他图表元素（如图形）提供更多空间。
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
