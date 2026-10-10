---
title: "Aspose::Words::NodeCollection class"
linktitle: "NodeCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeCollection class. Representerar en samling av noder av en specifik typ. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 43000
url: /sv/cpp/aspose.words/nodecollection/
---
## NodeCollection class


Representerar en samling noder av en specifik typ. För att lära dig mer, besök dokumentationsartikeln [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) i dokumentationen.

```cpp
class NodeCollection : public Aspose::Words::INodeCollection,
                       public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Lägger till en nod i slutet av samlingen. |
| [Clear](./clear/)() | Tar bort alla noder från denna samling och från dokumentet. |
| [Contains](./contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Avgör om en nod finns i samlingen. |
| [get_Count](./get_count/)() | Hämtar antalet noder i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Tillhandahåller en enkel "foreach"‑liknande iteration över samlingen av noder. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar en nod vid det angivna indexet. |
| [IndexOf](./indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Infogar en nod i samlingen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort noden på det angivna indexet från samlingen och från dokumentet. |
| [ToArray](./toarray/)() | Kopierar alla noder från samlingen till en ny nodarray. |
| static [Type](./type/)() |  |
## Anmärkningar


[NodeCollection](./) does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

[NodeCollection](./) supports indexed access, iteration and provides add and remove methods.

Den [NodeCollection](./) samlingen är "live", d.v.s. ändringar i barnen till nodobjektet som den skapades från återspeglas omedelbart i noderna som returneras av [NodeCollection](./) egenskaper och metoder.

[NodeCollection](./) is returned by [GetChildNodes()](../compositenode/getchildnodes/) and also serves as a base class for typed node collections such as [SectionCollection](../sectioncollection/), [ParagraphCollection](../paragraphcollection/) etc.

[NodeCollection](./) can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.

## Exempel



Visar hur man ersätter alla textrutefigurer med bildfigurer.
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

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
