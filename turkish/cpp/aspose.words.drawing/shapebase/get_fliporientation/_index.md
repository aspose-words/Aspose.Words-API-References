---
title: "Aspose::Words::Drawing::ShapeBase::get_FlipOrientation yöntemi"
linktitle: "get_FlipOrientation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_FlipOrientation yöntemi. C++'ta bir şeklin yönünü değiştirir."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.drawing/shapebase/get_fliporientation/
---
## ShapeBase::get_FlipOrientation method


Bir şeklin yönünü değiştirir.

```cpp
Aspose::Words::Drawing::FlipOrientation Aspose::Words::Drawing::ShapeBase::get_FlipOrientation()
```

## Açıklamalar


Varsayılan değer [None](../../fliporientation/).

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

* Enum [FlipOrientation](../../fliporientation/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
