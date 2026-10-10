---
title: "Aspose::Words::Drawing::WrapSide enum"
linktitle: "WrapSide"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::WrapSide enum. Metnin C++'da şeklin veya resmin hangi taraf(lar)ında dolandığını belirtir."
type: docs
weight: 44000
url: /tr/cpp/aspose.words.drawing/wrapside/
---
## WrapSide enum


Metnin şeklin veya resmin hangi taraf(lar)ında kaydırılacağını belirtir.

```cpp
enum class WrapSide
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Both | 0 | Belge metni şeklin her iki tarafında da dolanır. |
| Sol | 1 | Belge metni yalnızca şeklin sol tarafında dolanır. Şeklin sağ tarafında metin boş alanı vardır. |
| Sağ | 2 | Belge metni yalnızca şeklin sağ tarafında dolanır. Şeklin sol tarafında metin boş alanı vardır. |
| Largest | 3 | Belge metni, sayfa kenarından en uzak olan şekil tarafında dolanır ve şeklin diğer tarafında metin boş alanı bırakır. |
| Default | n/a | Varsayılan değer [Both](./)’dir. |


## Örnekler



Tüm metin kutusu şekillerinin görüntü şekilleriyle nasıl değiştirileceğini gösterir.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
