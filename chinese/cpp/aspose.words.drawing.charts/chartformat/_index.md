---
title: "Aspose::Words::Drawing::Charts::ChartFormat 类"
linktitle: "ChartFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartFormat 类。表示图表元素的格式。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


表示图表元素的格式。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Fill](./get_fill/)() | 获取父图表元素的填充格式。 |
| [get_IsDefined](./get_isdefined/)() | 获取指示是否已定义任何格式的标志。 |
| [get_ShapeType](./get_shapetype/)() | 获取或设置父图表元素的形状类型。 |
| [get_Stroke](./get_stroke/)() | 获取父图表元素的线条格式。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | 设置 [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/)。 |
| [SetDefaultFill](./setdefaultfill/)() | 将图表元素的填充重置为默认值。 |
| static [Type](./type/)() |  |

## 示例



展示如何使用图表格式化。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 删除默认生成的系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// 格式化图表背景。
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// 隐藏坐标轴刻度标签。
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// 格式化图表标题。
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// 格式化坐标轴标题。
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// 格式化图例。
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
