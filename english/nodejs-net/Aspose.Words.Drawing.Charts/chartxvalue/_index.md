---
title: ChartXValue class
linktitle: ChartXValue class
articleTitle: ChartXValue class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartXValue class. Represents an X value for a chart series."
type: docs
weight: 400
url: /nodejs-net/aspose.words.drawing.charts/chartxvalue/
---

## ChartXValue class

Represents an X value for a chart series.


### Remarks

This class contains a number of static methods for creating an X value of a particular type. The
[ChartXValue.valueType](./valueType/) property allows you to determine the type of an existing X value.

All non-null X values of a chart series must be of the same [ChartXValueType](../chartxvaluetype/) type.




### Properties

| Name | Description |
| --- | --- |
| [dateTimeValue](./dateTimeValue/) | Gets the stored datetime value. |
| [doubleValue](./doubleValue/) | Gets the stored numeric value. |
| [multilevelValue](./multilevelValue/) | Gets the stored multilevel value. |
| [stringValue](./stringValue/) | Gets the stored string value. |
| [timeValue](./timeValue/) | Gets the stored time value. |
| [valueType](./valueType/) | Gets the type of the X value stored in the object. |

### Methods

| Name | Description |
| --- | --- |
|[ fromDateTime(value)](./fromDateTime/#date) | Creates a [ChartXValue](./) instance of the [ChartXValueType.DateTime](../chartxvaluetype/#DateTime) type. |
|[ fromDouble(value)](./fromDouble/#number) | Creates a [ChartXValue](./) instance of the [ChartXValueType.Double](../chartxvaluetype/#Double) type. |
|[ fromMultilevelValue(value)](./fromMultilevelValue/#chartmultilevelvalue) | Creates a [ChartXValue](./) instance of the [ChartXValueType.Multilevel](../chartxvaluetype/#Multilevel) type. |
|[ fromString(value)](./fromString/#string) | Creates a [ChartXValue](./) instance of the [ChartXValueType.String](../chartxvaluetype/#String) type. |
|[ fromTimeSpan(value)](./fromTimeSpan/#unknown) | Creates a [ChartXValue](./) instance of the [ChartXValueType.Time](../chartxvaluetype/#Time) type. |

### See Also

* module [Aspose.Words.Drawing.Charts](../)

