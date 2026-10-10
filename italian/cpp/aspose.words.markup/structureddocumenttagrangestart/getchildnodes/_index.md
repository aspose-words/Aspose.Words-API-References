---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes metodo"
linktitle: "GetChildNodes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes metodo. Restituisce una collezione live di nodi figlio che corrispondono ai tipi specificati in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart::GetChildNodes method


Restituisce una collezione live di nodi figlio che corrispondono ai tipi specificati.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


## Esempi



Mostra come ottenere i nodi figlio di [StructuredDocumentTagRangeStart](../).
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

## Vedi anche

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
