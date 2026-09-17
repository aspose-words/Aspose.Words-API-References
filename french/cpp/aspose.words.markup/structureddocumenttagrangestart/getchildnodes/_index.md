---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes méthode"
linktitle: "GetChildNodes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes méthode. Retourne une collection dynamique de nœuds enfants correspondant aux types spécifiés en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart::GetChildNodes method


Renvoie une collection en direct des nœuds enfants correspondant aux types spécifiés.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


## Exemples



Montre comment obtenir les nœuds enfants de [StructuredDocumentTagRangeStart](../).
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

## Voir aussi

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
