---
title: Clear
second_title: Aspose.Words for C++ API Reference
description: Removes all nodes from this collection and from the document.
type: docs
weight: 27
url: /cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


Removes all nodes from this collection and from the document.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## Examples



Shows how to remove all sections from a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

// This document has one section with a few child nodes containing and displaying all the document's contents.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// Clear the collection of sections, which will remove all of the document's children.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(NodeType::Any, true)->get_Count());
ASSERT_EQ(String::Empty, doc->GetText().Trim());
```

## See Also

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
