---
title: "Aspose::Words::Drawing::Charts::Chart 类"
linktitle: "图表"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::Chart 类。提供对图表形状属性的访问。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


提供对图表形状属性的访问。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Axes](./get_axes/)() | 获取此图表的所有坐标轴集合。 |
| [get_AxisX](./get_axisx/)() | 提供对图表主 X 轴属性的访问。 |
| [get_AxisY](./get_axisy/)() | 提供对图表主 Y 轴属性的访问。 |
| [get_AxisZ](./get_axisz/)() | 提供对图表 Z 轴属性的访问。 |
| [get_DataTable](./get_datatable/)() | 提供对本图表数据表属性的访问。可以使用 [Show](../chartdatatable/get_show/) 属性显示数据表。 |
| [get_Format](./get_format/)() | 提供对图表填充和线条格式的访问。 |
| [get_Legend](./get_legend/)() | 提供对图表图例属性的访问。 |
| [get_Series](./get_series/)() | 提供对系列集合的访问。 |
| [get_SeriesGroups](./get_seriesgroups/)() | 提供对本图表系列组集合的访问。 |
| [get_SourceFullName](./get_sourcefullname/)() | 获取此图表所链接的 xls/xlsx 文件的路径和名称。 |
| [get_Style](./get_style/)() | 获取图表的样式。 |
| [get_Title](./get_title/)() | 提供对图表标题属性的访问。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/) 的 setter。 |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | 设置图表的样式。 |
| static [Type](./type/)() |  |

## 示例



展示如何插入图表并设置标题。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用文档生成器插入图表形状并获取其图表。
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// 使用 "Title" 属性为我们的图表添加标题，标题显示在图表区域的顶部中心。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// 将 "Show" 属性设置为 "true"，使标题可见。
title->set_Show(true);

// 将 "Overlay" 属性设置为 "true"，通过允许标题被覆盖，为其他图表元素提供更多空间。
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
