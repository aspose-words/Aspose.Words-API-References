---
title: "Aspose::Words::Drawing::WrapSide enum"
linktitle: "WrapSide"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::WrapSide enum. Specifica su quale lato (i) della forma o dell'immagine il testo avvolge in C++."
type: docs
weight: 44000
url: /it/cpp/aspose.words.drawing/wrapside/
---
## WrapSide enum


Specifica su quale lato (o lati) della forma o dell'immagine il testo avvolge.

```cpp
enum class WrapSide
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Entrambi | 0 | Il testo del documento si avvolge su entrambi i lati della forma. |
| Sinistra | 1 | Il testo del documento si avvolge solo sul lato sinistro della forma. C'è un'area libera dal testo sul lato destro della forma. |
| Destra | 2 | Il testo del documento si avvolge solo sul lato destro della forma. C'è un'area libera dal testo sul lato sinistro della forma. |
| Massimo | 3 | Il testo del documento si avvolge sul lato della forma più distante dal margine della pagina, lasciando un'area libera dal testo sull'altro lato della forma. |
| Default | n/a | Il valore predefinito è [Entrambi](./). |


## Esempi



Mostra come sostituire tutte le forme di casella di testo con forme immagine.
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

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
