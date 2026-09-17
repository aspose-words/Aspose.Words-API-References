---
title: "Aspose::Words::NodeCollection classe"
linktitle: "NodeCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NodeCollection classe. Représente une collection de nœuds d'un type spécifique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 43000
url: /fr/cpp/aspose.words/nodecollection/
---
## NodeCollection class


Représente une collection de nœuds d'un type spécifique. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeCollection : public Aspose::Words::INodeCollection,
                       public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ajoute un nœud à la fin de la collection. |
| [Clear](./clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](./contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Détermine si un nœud se trouve dans la collection. |
| [get_Count](./get_count/)() | Obtient le nombre de nœuds dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Fournit une itération simple de type "foreach" sur la collection de nœuds. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Récupère un nœud à l'index donné. |
| [IndexOf](./indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index basé sur zéro du nœud spécifié. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Insère un nœud dans la collection à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Supprime le nœud de la collection et du document. |
| [RemoveAt](./removeat/)(int32_t) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](./toarray/)() | Copie tous les nœuds de la collection dans un nouveau tableau de nœuds. |
| static [Type](./type/)() |  |
## Remarques


[NodeCollection](./) does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

[NodeCollection](./) supports indexed access, iteration and provides add and remove methods.

La collection [NodeCollection](./) est "live", c.-à-d. les modifications apportées aux enfants de l'objet nœud à partir duquel elle a été créée sont immédiatement reflétées dans les nœuds renvoyés par les propriétés et méthodes du [NodeCollection](./).

[NodeCollection](./) is returned by [GetChildNodes()](../compositenode/getchildnodes/) and also serves as a base class for typed node collections such as [SectionCollection](../sectioncollection/), [ParagraphCollection](../paragraphcollection/) etc.

[NodeCollection](./) can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.

## Exemples



Montre comment remplacer toutes les formes de zone de texte par des formes d'image.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Textboxes in drawing canvas.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(3, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox;
}))));
ASSERT_EQ(1, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::Image;
}))));

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    if (shape->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox)
    {
        auto replacementShape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
        replacementShape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");
        replacementShape->set_Left(shape->get_Left());
        replacementShape->set_Top(shape->get_Top());
        replacementShape->set_Width(shape->get_Width());
        replacementShape->set_Height(shape->get_Height());
        replacementShape->set_RelativeHorizontalPosition(shape->get_RelativeHorizontalPosition());
        replacementShape->set_RelativeVerticalPosition(shape->get_RelativeVerticalPosition());
        replacementShape->set_HorizontalAlignment(shape->get_HorizontalAlignment());
        replacementShape->set_VerticalAlignment(shape->get_VerticalAlignment());
        replacementShape->set_WrapType(shape->get_WrapType());
        replacementShape->set_WrapSide(shape->get_WrapSide());

        shape->get_ParentNode()->InsertAfter<System::SharedPtr<Aspose::Words::Drawing::Shape>>(replacementShape, shape);
        shape->Remove();
    }
}

shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(0, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox;
}))));
ASSERT_EQ(4, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::Image;
}))));

doc->Save(get_ArtifactsDir() + u"Shape.ReplaceTextboxesWithImages.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
