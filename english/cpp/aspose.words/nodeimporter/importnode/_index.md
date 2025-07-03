---
title: Aspose::Words::NodeImporter::ImportNode method
linktitle: ImportNode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeImporter::ImportNode method. Imports a node from one document into another in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Imports a node from one document into another.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to import. |
| isImportChildren | bool | **true** to import all child nodes recursively; otherwise, **false**. |

### ReturnValue

The cloned, imported node. The node belongs to the destination document, but has no parent.
## Remarks


Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [InsertBefore1()</see> or <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

## See Also

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
