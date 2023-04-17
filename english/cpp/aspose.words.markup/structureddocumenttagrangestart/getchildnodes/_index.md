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
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)
```


## Examples



Shows how to get child nodes of [StructuredDocumentTagRangeStart](../). 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Multi-section structured document tags.docx");
auto tag =
    System::DynamicCast_noexcept<StructuredDocumentTagRangeStart>(doc->GetChildNodes(NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << "\t|Child nodes count: " << tag->get_ChildNodes()->get_Count() << "\n" << std::endl;

for (const auto& node : System::IterateOver(tag->get_ChildNodes()))
{
    std::cout << String::Format(u"\t|Child node type: {0}", node->get_NodeType()) << std::endl;
}

for (const auto& node : System::IterateOver(tag->GetChildNodes(NodeType::Run, true)))
{
    std::cout << "\t|Child node text: " << node->GetText() << std::endl;
}
```

## See Also

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
