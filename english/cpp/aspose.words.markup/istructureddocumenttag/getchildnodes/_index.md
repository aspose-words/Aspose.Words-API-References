---
title: Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes method
linktitle: GetChildNodes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes method. Returns a live collection of child nodes that match the specified types in C++.'
type: docs
weight: 14500
url: /cpp/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag::GetChildNodes method


Returns a live collection of child nodes that match the specified types.

```cpp
virtual System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)=0
```


## Examples



Shows how to remove structured document tag, but keeps content inside. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// This collection provides a unified interface for accessing ranged and non-ranged structured tags.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## See Also

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
