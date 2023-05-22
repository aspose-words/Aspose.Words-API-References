---
title: Aspose::Words::Drawing::Charts::ChartXValueCollection class
linktitle: ChartXValueCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartXValueCollection class. Represents a collection of X values for a chart series in C++.'
type: docs
weight: 18400
url: /cpp/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class


Represents a collection of X values for a chart series.

```cpp
class ChartXValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue>>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() | Gets the number of items in this collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gets or sets the X value at the specified index. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Gets or sets the X value at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarks


All items of the collection other than **null** must have the same [ValueType](../chartxvalue/get_valuetype/).

The collection allows only changing X values. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../chartseries/) class can be used.

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
