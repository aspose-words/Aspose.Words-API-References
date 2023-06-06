---
title: Aspose::Words::Drawing::Charts::ChartYValue class
linktitle: ChartYValue
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartYValue class. Represents an Y value for a chart series in C++.'
type: docs
weight: 18600
url: /cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


Represents an Y value for a chart series.

```cpp
class ChartYValue : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Gets a flag indicating whether the specified object is equal to the current Y value object. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Creates a [ChartYValue](./) instance of the [DateTime](../chartyvaluetype/) type. |
| static [FromDouble](./fromdouble/)(double) | Creates a [ChartYValue](./) instance of the [Double](../chartyvaluetype/) type. |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Creates a [ChartYValue](./) instance of the [Time](../chartyvaluetype/) type. |
| [get_DateTimeValue](./get_datetimevalue/)() const | Gets the stored datetime value. |
| [get_DoubleValue](./get_doublevalue/)() const | Gets the stored numeric value. |
| [get_TimeValue](./get_timevalue/)() const | Gets the stored time value. |
| [get_ValueType](./get_valuetype/)() const | Gets the type of the Y value stored in the object. |
| [GetHashCode](./gethashcode/)() const override | Gets a hash code for the current Y value object. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarks


This class contains a number of static methods for creating an Y value of a particular type. The [ValueType](./get_valuetype/) property allows you to determine the type of an existing Y value.

All non-null Y values of a chart series must be of the same [ChartYValueType](../chartyvaluetype/) type. 
## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
