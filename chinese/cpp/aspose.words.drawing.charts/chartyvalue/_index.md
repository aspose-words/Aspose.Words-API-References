---
title: "Aspose::Words::Drawing::Charts::ChartYValue class"
linktitle: "ChartYValue"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartYValue class. 表示 C++ 中图表系列的 Y 值。"
type: docs
weight: 18600
url: /zh/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


表示图表系列的 Y 值。

```cpp
class ChartYValue : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 获取一个标志，指示指定的对象是否等于当前的 Y 值对象。 |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | 创建一个 [ChartYValue](./) 实例，类型为 [DateTime](../chartyvaluetype/)。 |
| static [FromDouble](./fromdouble/)(double) | 创建一个 [ChartYValue](./) 实例，类型为 [Double](../chartyvaluetype/)。 |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | 创建一个 [ChartYValue](./) 实例，类型为 [Time](../chartyvaluetype/)。 |
| [get_DateTimeValue](./get_datetimevalue/)() const | 获取存储的日期时间值。 |
| [get_DoubleValue](./get_doublevalue/)() const | 获取存储的数值。 |
| [get_TimeValue](./get_timevalue/)() const | 获取存储的时间值。 |
| [get_ValueType](./get_valuetype/)() const | 获取对象中存储的 Y 值的类型。 |
| [GetHashCode](./gethashcode/)() const override | 获取当前 Y 值对象的哈希码。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 备注


此类包含许多用于创建特定类型 Y 值的静态方法。 [ValueType](./get_valuetype/) 属性允许您确定现有 Y 值的类型。

图表系列的所有非空 Y 值必须具有相同的 [ChartYValueType](../chartyvaluetype/) 类型。
## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
