---
title: Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_ChildNodes method
linktitle: get_ChildNodes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_ChildNodes method. Gets all nodes between this range start node and the range end node in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/get_childnodes/
---
## StructuredDocumentTagRangeStart::get_ChildNodes method


Gets all nodes between this range start node and the range end node.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_ChildNodes()
```


## Examples



Shows how to get child nodes of [StructuredDocumentTagRangeStart](../). 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Multi-section structured document tags.docx");
auto tag =
    System::AsCast<StructuredDocumentTagRangeStart>(doc->GetChildNodes(NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << "\t|Child nodes count: " << tag->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() << "\n" << std::endl;

for (const auto& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Any, false)))
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
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
