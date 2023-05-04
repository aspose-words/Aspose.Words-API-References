---
title: ChartYValue Class
linktitle: ChartYValue
articleTitle: ChartYValue
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartYValue class. Represents an Y value for a chart series in C#.
type: docs
weight: 840
url: /net/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class

Represents an Y value for a chart series.

```csharp
public class ChartYValue
```

## Properties

| Name | Description |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartyvalue/datetimevalue/) { get; } | Gets the stored datetime value. |
| [DoubleValue](../../aspose.words.drawing.charts/chartyvalue/doublevalue/) { get; } | Gets the stored numeric value. |
| [TimeValue](../../aspose.words.drawing.charts/chartyvalue/timevalue/) { get; } | Gets the stored time value. |
| [ValueType](../../aspose.words.drawing.charts/chartyvalue/valuetype/) { get; } | Gets the type of the Y value stored in the object. |

## Methods

| Name | Description |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartyvalue/fromdatetime/)(*DateTime*) | Creates a `ChartYValue` instance of the DateTime type. |
| static [FromDouble](../../aspose.words.drawing.charts/chartyvalue/fromdouble/)(*double*) | Creates a `ChartYValue` instance of the Double type. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartyvalue/fromtimespan/)(*TimeSpan*) | Creates a `ChartYValue` instance of the Time type. |
| override [Equals](../../aspose.words.drawing.charts/chartyvalue/equals/)(*object*) | Gets a flag indicating whether the specified object is equal to the current Y value object. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartyvalue/gethashcode/)() | Gets a hash code for the current Y value object. |

## Remarks

This class contains a number of static methods for creating an Y value of a particular type. The [`ValueType`](./valuetype/) property allows you to determine the type of an existing Y value.

All non-null Y values of a chart series must be of the same [`ChartYValueType`](../chartyvaluetype/) type.

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
