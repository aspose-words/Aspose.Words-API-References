---
title: Aspose::Words::Drawing::Charts::ChartXValue class
linktitle: ChartXValue
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartXValue class. Represents an X value for a chart series in C++.'
type: docs
weight: 18200
url: /cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


Represents an X value for a chart series.

```cpp
class ChartXValue : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Gets a flag indicating whether the specified object is equal to the current X value object. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Creates a [ChartXValue](./) instance of the [DateTime](../chartxvaluetype/) type. |
| static [FromDouble](./fromdouble/)(double) | Creates a [ChartXValue](./) instance of the [Double](../chartxvaluetype/) type. |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | Creates a [ChartXValue](./) instance of the [Multilevel](../chartxvaluetype/) type. |
| static [FromString](./fromstring/)(const System::String\&) | Creates a [ChartXValue](./) instance of the [String](../chartxvaluetype/) type. |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Creates a [ChartXValue](./) instance of the [Time](../chartxvaluetype/) type. |
| [get_DateTimeValue](./get_datetimevalue/)() const | Gets the stored datetime value. |
| [get_DoubleValue](./get_doublevalue/)() const | Gets the stored numeric value. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | Gets the stored multilevel value. |
| [get_StringValue](./get_stringvalue/)() const | Gets the stored string value. |
| [get_TimeValue](./get_timevalue/)() const | Gets the stored time value. |
| [get_ValueType](./get_valuetype/)() const | Gets the type of the X value stored in the object. |
| [GetHashCode](./gethashcode/)() const override | Gets a hash code for the current X value object. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarks


This class contains a number of static methods for creating an X value of a particular type. The [ValueType](./get_valuetype/) property allows you to determine the type of an existing X value.

All non-null X values of a chart series must be of the same [ChartXValueType](../chartxvaluetype/) type. 
## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
