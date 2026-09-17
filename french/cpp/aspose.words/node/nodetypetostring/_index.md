---
title: "Aspose::Words::Node::NodeTypeToString méthode"
linktitle: "NodeTypeToString"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Node::NodeTypeToString méthode. Une méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words/node/nodetypetostring/
---
## Node::NodeTypeToString method


Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale.

```cpp
static System::String Aspose::Words::Node::NodeTypeToString(Aspose::Words::NodeType nodeType)
```


## Exemples



Montre comment utiliser la propriété NextSibling d'un nœud pour énumérer ses enfants immédiats.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

for (System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    std::cout << std::endl;
    std::cout << System::String::Format(u"Node type: {0}", Aspose::Words::Node::NodeTypeToString(node->get_NodeType())) << std::endl;

    System::String contents = node->GetText().Trim();
    std::cout << (contents == System::String::Empty ? u"This node contains no text" : System::String::Format(u"Contents: \"{0}\"", node->GetText().Trim())) << std::endl;
}
```

## Voir aussi

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
