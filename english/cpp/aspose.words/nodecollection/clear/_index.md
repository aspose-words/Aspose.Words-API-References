---
title: Aspose::Words::NodeCollection::Clear method
linktitle: Clear
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeCollection::Clear method. Removes all nodes from this collection and from the document in C++.'
type: docs
weight: 3000
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
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));

// This document has one section with a few child nodes containing and displaying all the document's contents.
ASSERT_EQ(doc->get_Sections()->get_Count(), 1);
ASSERT_EQ(doc->get_Sections()->idx_get(0)->GetChildNodes(NodeType::Any, true)->get_Count(), 17);
ASSERT_EQ(doc->GetText().Trim(), u"Hello World!\r\rHello Word!\r\r\rHello World!");

// Clear the collection of sections, which will remove all of the document's children.
doc->get_Sections()->Clear();

ASSERT_EQ(doc->GetChildNodes(NodeType::Any, true)->get_Count(), 0);
ASSERT_EQ(doc->GetText().Trim(), System::String::Empty);
```
## See Also

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
