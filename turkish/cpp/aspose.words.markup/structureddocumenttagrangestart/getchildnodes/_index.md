---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes method"
linktitle: "GetChildNodes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes method. C++'de belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart::GetChildNodes method


Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


## Örnekler



[StructuredDocumentTagRangeStart](../) alt düğümlerinin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Child nodes count: {0}\n", tag->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count()) << std::endl;

for (auto&& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Any, false)))
{
    std::cout << System::String::Format(u"\t|Child node type: {0}", node->get_NodeType()) << std::endl;
}

for (auto&& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    std::cout << System::String::Format(u"\t|Child node text: {0}", node->GetText()) << std::endl;
}
```

## Ayrıca Bakınız

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
