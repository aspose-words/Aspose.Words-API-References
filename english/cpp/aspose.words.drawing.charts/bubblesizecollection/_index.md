---
title: Aspose::Words::Drawing::Charts::BubbleSizeCollection class
linktitle: BubbleSizeCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::BubbleSizeCollection class. Represents a collection of bubble sizes for a chart series in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


Represents a collection of bubble sizes for a chart series.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() | Gets the number of items in this collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gets or sets the bubble size value at the specified index. |
| [idx_set](./idx_set/)(int32_t, double) | Gets or sets the bubble size value at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarks


The collection allows only changing bubble sizes. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../chartseries/) class can be used.

Empty bubble size values are represented as **NaN**.

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
