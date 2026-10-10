---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels 类"
linktitle: "AxisTickLabels"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels 类。表示 C++ 中坐标轴刻度标签的属性。"
type: docs
weight: 3250
url: /zh/cpp/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class


表示轴刻度标记标签的属性。

```cpp
class AxisTickLabels : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Alignment](./get_alignment/)() | 获取或设置坐标轴刻度标签的文本对齐方式。 |
| [get_Font](./get_font/)() | 提供对刻度标签字体格式的访问。 |
| [get_IsAutoSpacing](./get_isautospacing/)() | 获取或设置一个标志，指示是否使用自动间隔来绘制刻度标签。 |
| [get_Offset](./get_offset/)() | 获取或设置刻度标签距坐标轴的距离。 |
| [get_Orientation](./get_orientation/)() | 获取或设置刻度标签文本的方向。 |
| [get_Position](./get_position/)() | 获取或设置刻度标签在坐标轴上的位置。 |
| [get_Rotation](./get_rotation/)() | 获取或设置刻度标签的旋转角度（以度为单位）。 |
| [get_Spacing](./get_spacing/)() | 获取或设置绘制刻度标签的间隔。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | 用于设置 [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Alignment](./get_alignment/)。 |
| [set_IsAutoSpacing](./set_isautospacing/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::AxisTickLabels::get_IsAutoSpacing](./get_isautospacing/)。 |
| [set_Offset](./set_offset/)(int32_t) | 用于设置 [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Offset](./get_offset/)。 |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | 用于设置 [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation](./get_orientation/)。 |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::AxisTickLabelPosition) | 用于设置 [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Position](./get_position/)。 |
| [set_Rotation](./set_rotation/)(int32_t) | 用于设置 [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation](./get_rotation/)。 |
| [set_Spacing](./set_spacing/)(int32_t) | 用于设置 [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Spacing](./get_spacing/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何插入图表并修改其轴的外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 为 X 轴插入带有类别的图表系列，并为 Y 轴提供相应的数值。
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// 图表轴具有多种可更改其外观的选项，
// 例如其方向、主/次单位刻度和刻度标记。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// 柱形图没有 Z 轴。
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
