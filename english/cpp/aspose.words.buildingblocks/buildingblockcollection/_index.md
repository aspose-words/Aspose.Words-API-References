---
title: Aspose::Words::BuildingBlocks::BuildingBlockCollection class
linktitle: BuildingBlockCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::BuildingBlockCollection class. A collection of BuildingBlock objects in the document. To learn more, visit the Aspose.Words Document Object Model (DOM) (https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


A collection of [BuildingBlock](../buildingblock/) objects in the document. 
To learn more, visit the Aspose.Words Document Object Model (DOM) (https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```cpp
class BuildingBlockCollection : public NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [ToArray](./toarray/)() | Copies all building blocks from the collection to a new array of building blocks. |
| static [Type](./type/)() |  |
| [idx_get](./idx_get/)(int32_t) | Retrieves a building block at the given index. |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Determines whether a node is in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](../../aspose.words/nodecollection/gettype/)() const override |  |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts a node into the collection at the specified index. |
| [Is](../../aspose.words/nodecollection/is/)(const System::TypeInfo \&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copies all nodes from the collection to a new array of nodes. |
| static [Type](../../aspose.words/nodecollection/type/)() |  |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [idx_get](../../aspose.words/nodecollection/idx_get/)(int32_t) | Retrieves a node at the given index. |
## Remarks


You do not create instances of this class directly. To access a collection of building blocks use the [BuildingBlocks](../glossarydocument/get_buildingblocks/) property.
## See Also

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
