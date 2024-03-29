---
title: Aspose::Words::NodeList::idx_get method
linktitle: idx_get
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeList::idx_get method. Retrieves a node at the given index in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


Retrieves a node at the given index.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the list of nodes. |
## Remarks


The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## See Also

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
