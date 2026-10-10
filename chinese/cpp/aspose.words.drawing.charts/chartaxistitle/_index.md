---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle class"
linktitle: "ChartAxisTitle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle 类。提供对坐标轴标题属性的访问。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 5750
url: /zh/cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


提供对坐标轴标题属性的访问。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartAxisTitle : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Font](./get_font/)() | 提供对坐标轴标题字体格式的访问。 |
| [get_Format](./get_format/)() | 提供对坐标轴标题填充和线条格式的访问。 |
| [get_Orientation](./get_orientation/)() | 获取或设置坐标轴标题文本的方向。 |
| [get_Overlay](./get_overlay/)() | 确定是否允许其他图表元素覆盖标题。默认值为 **false**。 |
| [get_Rotation](./get_rotation/)() | 获取或设置坐标轴标题的旋转角度（以度为单位）。 |
| [get_Show](./get_show/)() | 确定是否在坐标轴上显示标题。默认值为 **false**。 |
| [get_Text](./get_text/)() | 获取或设置坐标轴标题的文本。如果指定 **null** 或空值，将显示自动生成的标题。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation](./get_orientation/)。 |
| [set_Overlay](./set_overlay/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/)。 |
| [set_Rotation](./set_rotation/)(int32_t) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation](./get_rotation/)。 |
| [set_Show](./set_show/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/)。 |
| [set_Text](./set_text/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何设置图表坐标轴标题。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// 删除默认生成的系列。
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
