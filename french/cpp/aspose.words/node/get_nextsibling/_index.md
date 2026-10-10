---
title: "Aspose::Words::Node::get_NextSibling méthode"
linktitle: "get_NextSibling"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Node::get_NextSibling méthode. Obtient le nœud immédiatement suivant ce nœud en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/node/get_nextsibling/
---
## Node::get_NextSibling method


Obtient le nœud immédiatement suivant ce nœud.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_NextSibling()
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
