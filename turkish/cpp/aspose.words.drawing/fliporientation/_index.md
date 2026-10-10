---
title: "Aspose::Words::Drawing::FlipOrientation enum"
linktitle: "FlipOrientation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::FlipOrientation enum. C++'da bir şeklin yönelimi için olası değerler."
type: docs
weight: 23000
url: /tr/cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


Bir şeklin yönelimi için olası değerler.

```cpp
enum class FlipOrientation
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Koordinatlar ters çevrilmemiştir. |
| Yatay | 1 | y ekseni boyunca ters çevir, x koordinatlarını tersine çevir. |
| Dikey | 2 | x ekseni boyunca ters çevir, y koordinatlarını tersine çevir. |
| Both | 3 | y ve x eksenlerinin her ikisi boyunca ters çevir. |


## Örnekler



Bir şekli bir eksende nasıl ters çevireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir resim şekli ekleyin ve yönelimini varsayılan durumunda bırakın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayarak ikinci şekli y ekseninde ters çevir,
// böylece ilk şeklin yatay bir ayna görüntüsü olur.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayarak üçüncü şekli x ekseninde ters çevir,
// böylece ilk şeklin dikey bir ayna görüntüsü olur.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayarak dördüncü şekli hem x hem y eksenlerinde ters çevir,
// böylece ilk şeklin hem yatay hem dikey ayna görüntüsü olur.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
