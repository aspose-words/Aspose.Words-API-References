---
title: "Aspose::Words::Drawing::Charts::AxisBound 类"
linktitle: "AxisBound"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::AxisBound 类。表示轴值的最小或最大界限。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


表示轴值的最小或最大界限。欲了解更多信息，请访问 [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) 文档文章。

```cpp
class AxisBound : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [AxisBound](./axisbound/)() | 创建一个新实例，指示轴界限应由文字处理应用程序自动确定。 |
| [AxisBound](./axisbound/)(double) | 创建一个以数字表示的轴界限。 |
| [AxisBound](./axisbound/)(System::DateTime) | 创建一个以日期时间值表示的轴界限。 |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| [get_IsAuto](./get_isauto/)() const | 返回一个标志，指示轴界限应自动确定。 |
| [get_Value](./get_value/)() const | 返回轴界限的数值。 |
| [get_ValueAsDate](./get_valueasdate/)() | 返回以日期时间表示的轴界限值。 |
| [GetHashCode](./gethashcode/)() const override | 作为此类型的哈希函数。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | 返回一个用户友好的字符串，显示此对象的值。 |
| static [Type](./type/)() |  |
## 备注


界限可以指定为数值、日期时间或特殊的 "auto" 值。

此类的实例是不可变的。

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
