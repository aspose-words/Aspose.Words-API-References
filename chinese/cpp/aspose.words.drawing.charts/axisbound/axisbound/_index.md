---
title: "Aspose::Words::Drawing::Charts::AxisBound::AxisBound constructor"
linktitle: "AxisBound"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::AxisBound::AxisBound constructor. 创建一个新实例，指示坐标轴范围应由 C++ 中的文字处理应用程序自动确定。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound::AxisBound() constructor


创建一个新实例，指示轴界限应由文字处理应用程序自动确定。

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound()
```


## 示例



展示如何设置自定义轴范围。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 添加一个包含两个十进制数组的系列。第一个数组包含 X 值，
// 第二个数组包含散点图中点的对应 Y 值。
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), System::MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// 默认情况下，默认缩放会应用于图表的 X 和 Y 轴，
// 这样它们的范围足够大，能够容纳每个系列的所有 X 和 Y 值。
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// 我们可以定义自己的坐标轴范围。
// 在这种情况下，我们将让 X 轴和 Y 轴的刻度显示 0 到 10 的范围。
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// 创建一个折线图，其中系列在 X 轴上需要日期范围，Y 轴上需要小数值。
chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

System::ArrayPtr<System::DateTime> dates = System::MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23), System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, System::MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// 我们也可以将坐标轴范围设置为日期形式，以限制图表的时间段。
// 将范围设置为 1980-1990 将省略系列中的两个值
// 这些值位于图表范围之外。
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(get_ArtifactsDir() + u"Charts.AxisBound.docx");
```

## 另见

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## AxisBound::AxisBound(double) constructor


创建一个以数字表示的轴界限。

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound(double value)
```


## 示例



展示如何插入包含日期/时间值的图表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 添加一个自定义系列，其中 X 轴包含日期/时间值，Y 轴包含相应的十进制值。
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// 设置 X 轴的下限和上限。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// 将 X 轴的主单位设置为一周，次单位设置为一天。
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// 为十进制值定义 Y 轴属性。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## 另见

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## AxisBound::AxisBound(System::DateTime) constructor


创建一个以日期时间值表示的轴界限。

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound(System::DateTime datetime)
```


## 示例



展示如何插入包含日期/时间值的图表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 添加一个自定义系列，其中 X 轴包含日期/时间值，Y 轴包含相应的十进制值。
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// 设置 X 轴的下限和上限。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// 将 X 轴的主单位设置为一周，次单位设置为一天。
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// 为十进制值定义 Y 轴属性。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## 另见

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
