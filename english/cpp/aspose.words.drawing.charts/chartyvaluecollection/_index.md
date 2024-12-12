---
title: Aspose::Words::Drawing::Charts::ChartYValueCollection class
linktitle: ChartYValueCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartYValueCollection class. Represents a collection of Y values for a chart series in C++.'
type: docs
weight: 18800
url: /cpp/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class


Represents a collection of Y values for a chart series.

```cpp
class ChartYValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue>>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() | Gets the number of items in this collection. |
| [get_FormatCode](./get_formatcode/)() | Gets or sets the format code applied to the Y values. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gets or sets the Y value at the specified index. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Gets or sets the Y value at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Setter for [Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Remarks


All items of the collection other than **null** must have the same [ValueType](../chartyvalue/get_valuetype/).

The collection allows only changing Y values. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../chartseries/) class can be used.

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
