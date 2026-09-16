---
title: "Aspose::Words::Drawing::Charts::AxisDisplayUnit::get_Document method"
linktitle: "get_Document"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::AxisDisplayUnit::get_Document 方法。返回包含父图表的文档（在 C++ 中）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.drawing.charts/axisdisplayunit/get_document/
---
## AxisDisplayUnit::get_Document method


返回包含父图表的文档。

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Drawing::Charts::AxisDisplayUnit::get_Document()
```


## 示例



展示如何操作图表坐标轴的刻度线和显示值。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// 将 Y 轴的次刻度线设置为指向绘图区域之外，
// 并将主刻度线设置为穿过坐标轴。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// 将 Y 轴设置为每 10 个单位显示一个主刻度，每 1 个单位显示一个次刻度。
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// 将 Y 轴的范围设置为 -10 到 20。
// 此 Y 轴现在将显示 4 个主刻度线和 27 个次刻度线。
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// 对于 X 轴，将主刻度线设置为每 10 个单位，
// 每个次刻度线设置为 2.5 个单位。
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// 配置两种刻度线，使其显示在图形绘图区内部。
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// 设置 X 轴范围，使 X 轴跨越 5 个主刻度线和 12 个次刻度线。
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// 将刻度标签设置为以百万为单位显示其数值。
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// 我们可以设置一个更具体的值，以便刻度标签显示其数值。
// 此语句等同于上面的语句。
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## 另见

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [AxisDisplayUnit](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
