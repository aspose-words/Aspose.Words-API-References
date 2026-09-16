---
title: "Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay 方法"
linktitle: "get_Overlay"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay 方法。确定是否允许其他图表元素覆盖图例。默认值在 C++ 中为 false。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.drawing.charts/chartlegend/get_overlay/
---
## ChartLegend::get_Overlay method


确定是否允许其他图表元素覆盖图例。默认值为 **false**。

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay() const
```


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

* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
