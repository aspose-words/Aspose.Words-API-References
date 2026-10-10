---
title: "Aspose::Words::Drawing::Charts::ChartDataTable class"
linktitle: "ChartDataTable"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataTable 类。允许在 C++ 中指定图表数据表的属性。"
type: docs
weight: 9500
url: /zh/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


允许指定图表数据表的属性。

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Font](./get_font/)() | 提供对数据表字体格式的访问。 |
| [get_Format](./get_format/)() | 提供对数据表文本背景填充和边框格式的访问。 |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | 获取或设置指示是否显示数据表水平边框的标志。默认值为 **true**。 |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | 获取或设置指示是否在数据表中显示图例键的标志。默认值为 **true**。 |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | 获取或设置指示是否显示轮廓边框（即围绕系列和类别名称的边框）的标志。默认值为 **true**。 |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | 获取或设置指示是否显示数据表垂直边框的标志。默认值为 **true**。 |
| [get_Show](./get_show/)() const | 获取或设置指示是否在图表中显示数据表的标志。默认值为 **false**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/) 的方法。 |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/) 的方法。 |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/) 的方法。 |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

## 示例



展示如何显示带有图表系列数据的数据表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();
auto xValues = System::MakeArray<double>({2020, 2021, 2022, 2023});
series->Add(u"Series1", xValues, System::MakeArray<double>({5, 11, 2, 7}));
series->Add(u"Series2", xValues, System::MakeArray<double>({6, 5.5, 7, 7.8}));
series->Add(u"Series3", xValues, System::MakeArray<double>({10, 8, 7, 9}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> dataTable = chart->get_DataTable();
dataTable->set_Show(true);

dataTable->set_HasLegendKeys(false);
dataTable->set_HasHorizontalBorder(false);
dataTable->set_HasVerticalBorder(false);
dataTable->set_HasOutlineBorder(false);

dataTable->get_Font()->set_Italic(true);
dataTable->get_Format()->get_Stroke()->set_Weight(1);
dataTable->get_Format()->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDot);
dataTable->get_Format()->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());

doc->Save(get_ArtifactsDir() + u"Charts.DataTable.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
