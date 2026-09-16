---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat class"
linktitle: "ChartNumberFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat 类。表示父元素的数字格式。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class


表示父元素的数字格式。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartNumberFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_FormatCode](./get_formatcode/)() | 获取或设置应用于数据标签的格式代码。 |
| [get_IsLinkedToSource](./get_islinkedtosource/)() | 指定格式代码是否链接到源单元格。默认值为 true。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode](./get_formatcode/) 的 setter。 |
| [set_IsLinkedToSource](./set_islinkedtosource/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource](./get_islinkedtosource/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何为图表值设置格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 向图表添加一个自定义系列，X 轴使用类别，
// 并为 Y 轴提供相应的大数值。
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// 设置 Y 轴刻度标签的数字格式，使其不使用逗号分组数字。
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// 此标志可以覆盖上述值，并从源单元格获取数字格式。
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
