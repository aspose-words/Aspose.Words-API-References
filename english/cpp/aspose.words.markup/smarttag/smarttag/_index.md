---
title: Aspose::Words::Markup::SmartTag::SmartTag constructor
linktitle: SmartTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::SmartTag::SmartTag constructor. Initializes a new instance of the SmartTag class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


Initializes a new instance of the [SmartTag](../) class.

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
## Remarks


When you create a new node, you need to specify a document to which the node belongs. A node cannot exist without a document because it depends on the document-wide structures such as lists and styles. Although a node always belongs to a document, a node might or might not be a part of the document tree.

When a node is created, it belongs to a document, but is not yet part of the document tree and [ParentNode](../../../aspose.words/node/get_parentnode/) is null. To insert a node into the document, use the [InsertAfter1()</see> or <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) methods on the parent node.

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
