---
title: "Méthode Aspose::Words::Node::Remove"
linktitle: "Supprimer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Node::Remove. Supprime lui‑même du parent en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words/node/remove/
---
## Node::Remove method


Se supprime du parent.

```cpp
void Aspose::Words::Node::Remove()
```


## Exemples



Montre comment supprimer toutes les formes avec des images d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));

for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        shape->Remove();
    }
}

ASSERT_EQ(0, shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));
```


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

## Voir aussi

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
