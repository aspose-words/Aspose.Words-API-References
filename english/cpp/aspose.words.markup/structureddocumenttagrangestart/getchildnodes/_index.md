---
title: Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes method
linktitle: GetChildNodes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes method. Returns a live collection of child nodes that match the specified types in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart::GetChildNodes method


Returns a live collection of child nodes that match the specified types.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


## Examples



Shows how to get child nodes of [StructuredDocumentTagRangeStart](../). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Multi-section structured document tags.docx"));
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));

System::Console::WriteLine(u"StructuredDocumentTagRangeStart values:");
System::Console::WriteLine(System::String::Format(u"\t|Child nodes count: {0}\n", tag->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count()));

for (auto&& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Any, false)))
{
    System::Console::WriteLine(System::String::Format(u"\t|Child node type: {0}", node->get_NodeType()));
}

for (auto&& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    System::Console::WriteLine(System::String::Format(u"\t|Child node text: {0}", node->GetText()));
}
```

## See Also

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
