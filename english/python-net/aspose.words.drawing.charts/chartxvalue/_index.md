---
title: ChartXValue class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents an X value for a chart series."
type: docs
weight: 320
url: /python-net/aspose.words.drawing.charts/chartxvalue/
---

## ChartXValue class

Represents an X value for a chart series.


This class contains a number of static methods for creating an X value of a particular type. The
[ChartXValue.value_type](./value_type/) property allows you to determine the type of an existing X value.

All non-null X values of a chart series must be of the same [ChartXValueType](../chartxvaluetype/) type.




### Properties

| Name | Description |
| --- | --- |
| [date_time_value](./date_time_value/) | Gets the stored datetime value. |
| [double_value](./double_value/) | Gets the stored numeric value. |
| [multilevel_value](./multilevel_value/) | Gets the stored multilevel value. |
| [string_value](./string_value/) | Gets the stored string value. |
| [time_value](./time_value/) | Gets the stored time value. |
| [value_type](./value_type/) | Gets the type of the X value stored in the object. |

### Methods

| Name | Description |
| --- | --- |
|[ from_date_time(value)](./from_date_time/#datetime) | Creates a [ChartXValue](./) instance of the [ChartXValueType.DATE_TIME](../chartxvaluetype/#DATE_TIME) type. |
|[ from_double(value)](./from_double/#float) | Creates a [ChartXValue](./) instance of the [ChartXValueType.DOUBLE](../chartxvaluetype/#DOUBLE) type. |
|[ from_multilevel_value(value)](./from_multilevel_value/#chartmultilevelvalue) | Creates a [ChartXValue](./) instance of the [ChartXValueType.MULTILEVEL](../chartxvaluetype/#MULTILEVEL) type. |
|[ from_string(value)](./from_string/#str) | Creates a [ChartXValue](./) instance of the [ChartXValueType.STRING](../chartxvaluetype/#STRING) type. |
|[ from_time_span(value)](./from_time_span/#unknown) | Creates a [ChartXValue](./) instance of the [ChartXValueType.TIME](../chartxvaluetype/#TIME) type. |

### See Also

* module [aspose.words.drawing.charts](../)

