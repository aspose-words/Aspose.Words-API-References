---
title: "Aspose::Words::Drawing::Charts::ChartLegend class"
linktitle: "ChartLegend"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartLegend 类。表示图表图例属性。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


表示图例属性。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Font](./get_font/)() | 提供对图例条目默认字体格式的访问。要覆盖特定图例条目的字体格式，请使用[Font](../chartlegendentry/get_font/)属性。 |
| [get_Format](./get_format/)() | 提供对图例填充和线条格式的访问。 |
| [get_LegendEntries](./get_legendentries/)() const | 返回父图表中所有系列和趋势线的图例条目集合。 |
| [get_Overlay](./get_overlay/)() const | 确定是否允许其他图表元素覆盖图例。默认值为 **false**。 |
| [get_Position](./get_position/)() | 指定图例在图表上的位置。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/) 的方法。 |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | 用于设置 [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/) 的方法。 |
| static [Type](./type/)() |  |

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
