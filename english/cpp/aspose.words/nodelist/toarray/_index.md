---
title: ToArray
second_title: Aspose.Words for C++ API Reference
description: Copies all nodes from the collection to a new array of nodes.
type: docs
weight: 53
url: /cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


Copies all nodes from the collection to a new array of nodes.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

An array of nodes.
## Remarks


You should not be adding/removing nodes while iterating over a collection of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy nodes into a fixed-size array and then iterate over the array.

## See Also

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
