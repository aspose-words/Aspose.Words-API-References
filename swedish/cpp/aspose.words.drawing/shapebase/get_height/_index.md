---
title: "Aspose::Words::Drawing::ShapeBase::get_Height metod"
linktitle: "get_Height"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Height metod. Hämtar eller anger höjden på formens innehållande block i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.drawing/shapebase/get_height/
---
## ShapeBase::get_Height method


Hämtar eller anger höjden på formens innehållande block.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Height()
```

## Anmärkningar


För en form på toppnivå är värdet i punkter.

För former i en grupp är värdet i koordinatrymden och enheterna för den överordnade gruppen.

Standardvärdet är 0.

## Exempel



Visar hur man infogar en flytande bild och anger dess position och storlek.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Konfigurera figurens egenskap "RelativeHorizontalPosition" så att den behandlar värdet av egenskapen "Left"
// som figurens horisontella avstånd, i punkter, från sidans vänstra kant.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Ställ in figurens horisontella avstånd från sidans vänstra kant till 100.
shape->set_Left(100);

// Använd egenskapen "RelativeVerticalPosition" på liknande sätt för att placera figuren 80pt under sidans övre kant.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Ställ in figurens höjd, vilket automatiskt skalar bredden för att bevara proportionerna.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Egenskaperna "Bottom" och "Right" innehåller bildens nedre och högra kanter.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```


Visar hur man ändrar storlek på en form med en bild.
```cpp
// När vi infogar en bild med metoden "InsertImage" skalar byggaren formen som visar bilden så att,
// när vi visar dokumentet med 100% zoom i Microsoft Word, visar formen bilden i dess faktiska storlek.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// En 400x400 bild kommer att skapa ett ImageData-objekt med en bildstorlek på 300x300pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Om en forms dimensioner matchar bilddataens dimensioner,
// så visar formen bilden i sin ursprungliga storlek.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Minska den totala storleken på formen med 50 %.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// Skalfaktorer gäller både för bredden och höjden samtidigt för att bevara formens proportioner.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// När vi ändrar storlek på formen förblir bilddataens storlek densamma.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Vi kan referera till bilddataens dimensioner för att tillämpa en skalning baserad på bildens storlek.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
