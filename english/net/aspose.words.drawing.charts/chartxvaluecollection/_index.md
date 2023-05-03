---
title: ChartXValueCollection Class
linktitle: ChartXValueCollection
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartXValueCollection class. Represents a collection of X values for a chart series in C#.
type: docs
weight: 820
url: /net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Represents a collection of X values for a chart series.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Gets the number of items in this collection. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Gets or sets the X value at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Returns an enumerator object. |

## Remarks

All items of the collection other than **null** must have the same [`ValueType`](../chartxvalue/valuetype/).

The collection allows only changing X values. To add or insert new values to a chart series, or remove values, the appropriate methods of the [`ChartSeries`](../chartseries/) class can be used.

### See Also

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartXValue](../chartxvalue/)
* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
