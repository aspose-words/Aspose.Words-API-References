---
title: Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes method
linktitle: GetChildNodes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes method. Returns a live collection of child nodes that match the specified type in C++.'
type: docs
weight: 34500
url: /cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


Returns a live collection of child nodes that match the specified type.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Specifies the type of nodes to select. |
| isDeep | bool | **true** to select from all child nodes recursively; **false** to select only among immediate children. |

### ReturnValue

A live collection of child nodes of the specified type.
## Remarks


The collection of nodes returned by this method is always live.

A live collection is always in sync with the document. For example, if you selected all sections in a document and enumerate through the collection deleting the sections, the section is removed from the collection immediately when it is removed from the document.

## See Also

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
