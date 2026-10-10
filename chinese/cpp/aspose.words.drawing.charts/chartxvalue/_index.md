---
title: "Aspose::Words::Drawing::Charts::ChartXValue 类"
linktitle: "ChartXValue"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartXValue 类。表示 C++ 中图表系列的 X 值。"
type: docs
weight: 18200
url: /zh/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


表示图表系列的 X 值。

```cpp
class ChartXValue : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 获取一个标志，指示指定的对象是否等于当前的 X 值对象。 |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | 创建一个 [ChartXValue](./) 实例，类型为 [DateTime](../chartxvaluetype/)。 |
| static [FromDouble](./fromdouble/)(double) | 创建一个 [ChartXValue](./) 实例，类型为 [Double](../chartxvaluetype/)。 |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | 创建一个 [ChartXValue](./) 实例，类型为 [Multilevel](../chartxvaluetype/)。 |
| static [FromString](./fromstring/)(const System::String\&) | 创建一个 [ChartXValue](./) 实例，类型为 [String](../chartxvaluetype/)。 |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | 创建一个 [ChartXValue](./) 实例，类型为 [Time](../chartxvaluetype/)。 |
| [get_DateTimeValue](./get_datetimevalue/)() const | 获取存储的日期时间值。 |
| [get_DoubleValue](./get_doublevalue/)() const | 获取存储的数值。 |
| [get_MultilevelValue](./get_multilevelvalue/)() const | 获取存储的多层值。 |
| [get_StringValue](./get_stringvalue/)() const | 获取存储的字符串值。 |
| [get_TimeValue](./get_timevalue/)() const | 获取存储的时间值。 |
| [get_ValueType](./get_valuetype/)() const | 获取对象中存储的 X 值的类型。 |
| [GetHashCode](./gethashcode/)() const override | 获取当前 X 值对象的哈希码。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 备注


此类包含多个用于创建特定类型 X 值的静态方法。 [ValueType](./get_valuetype/) 属性允许您确定现有 X 值的类型。

图表系列的所有非空 X 值必须具有相同的 [ChartXValueType](../chartxvaluetype/) 类型。

## 示例



展示如何使用数据填充图表系列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// 清除第一系列的 X 和 Y 值。
series1->ClearValues();

// 使用数据填充系列。
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// 清除第二系列的 X 和 Y 值。
series2->Clear();

// 使用数据填充系列。
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
