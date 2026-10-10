---
title: "Aspose::Words::Notes::FootnoteSeparator::get_NodeType méthode"
linktitle: "get_NodeType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::FootnoteSeparator::get_NodeType méthode. Obtient le type de ce nœud en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.notes/footnoteseparator/get_nodetype/
---
## FootnoteSeparator::get_NodeType method


Obtient le type de ce nœud.

```cpp
Aspose::Words::NodeType Aspose::Words::Notes::FootnoteSeparator::get_NodeType() const override
```


## Exemples



Montre comment supprimer tous les nœuds enfants d'un type spécifique d'un nœud composite.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Enregistrez le nœud frère suivant dans une variable au cas où nous voudrions nous y déplacer après avoir supprimé ce nœud.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // Un corps de section peut contenir des nœuds Paragraph et Table.
    // Si le nœud est un tableau, supprimez-le du parent.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```


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

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [FootnoteSeparator](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
