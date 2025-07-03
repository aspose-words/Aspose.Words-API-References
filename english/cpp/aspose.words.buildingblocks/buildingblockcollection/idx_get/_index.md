---
title: Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get method
linktitle: idx_get
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get method. Retrieves a building block at the given index in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.buildingblocks/buildingblockcollection/idx_get/
---
## BuildingBlockCollection::idx_get method


Retrieves a building block at the given index.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the list of building blocks. |
## Remarks


The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## See Also

* Class [BuildingBlock](../../buildingblock/)
* Class [BuildingBlockCollection](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
