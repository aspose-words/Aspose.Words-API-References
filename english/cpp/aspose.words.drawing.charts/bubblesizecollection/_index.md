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
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [get_Count](./get_count/)() | Gets the number of items in this collection. |
| [get_FormatCode](./get_formatcode/)() | Gets or sets the format code applied to the bubble sizes. |
| [idx_get](./idx_get/)(int32_t) | Gets or sets the bubble size value at the specified index. |
| [idx_set](./idx_set/)(int32_t, double) | Gets or sets the bubble size value at the specified index. |
| [set_FormatCode](./set_formatcode/)(const System::String \&) | Sets the format code applied to the bubble sizes. |
## Remarks


The collection allows only changing bubble sizes. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../chartseries/) class can be used.

Empty bubble size values are represented as **NaN**.
## See Also

* [Add()](../chartseries/add/)
* [Add()](../chartseries/add/)
* [Add()](../chartseries/add/)
* [Insert()](../chartseries/insert/)
* [Insert()](../chartseries/insert/)
* [Insert()](../chartseries/insert/)
* [Remove()](../chartseries/remove/)

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
