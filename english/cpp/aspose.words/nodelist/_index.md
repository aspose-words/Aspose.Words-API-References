---
title: Aspose::Words::NodeList class
linktitle: NodeList
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeList class. Represents a collection of nodes matching an XPath query executed using the SelectNodes() method. To learn more, visit the  documentation article in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words/nodelist/
---
## NodeList class


Represents a collection of nodes matching an XPath query executed using the [SelectNodes()](../) method. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() const | Gets the number of nodes in the list. |
| [GetEnumerator](./getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Retrieves a node at the given index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Copies all nodes from the collection to a new array of nodes. |
| static [Type](./type/)() |  |
## Remarks


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


Treat the [NodeList](./) collection as a "snapshot" collection. [NodeList](./) starts as a "live" collection because the nodes are not actually retrieved when the XPath query is run. The nodes are only retrieved upon access and at this time the node and all nodes that precede it are cached forming a "snapshot" collection. 

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
