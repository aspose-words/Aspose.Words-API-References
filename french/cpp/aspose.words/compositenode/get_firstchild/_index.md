---
title: "Aspose::Words::CompositeNode::get_FirstChild méthode"
linktitle: "get_FirstChild"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CompositeNode::get_FirstChild méthode. Obtient le premier enfant du nœud en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/compositenode/get_firstchild/
---
## CompositeNode::get_FirstChild method


Obtient le premier enfant du nœud.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_FirstChild() const
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

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
