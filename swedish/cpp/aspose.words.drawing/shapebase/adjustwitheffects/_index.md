---
title: "Aspose::Words::Drawing::ShapeBase::AdjustWithEffects‑metod"
linktitle: "AdjustWithEffects"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::AdjustWithEffects‑metod. Lägger till värden för effektutbredning till källrektangeln och returnerar den slutliga rektangeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase::AdjustWithEffects method


Lägger till värden för effektutbredning till källrektangeln och returnerar den slutliga rektangeln.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::AdjustWithEffects(System::Drawing::RectangleF source)
```


## Exempel



Visar hur man kontrollerar hur en formes gränser påverkas av formeffekter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// De två formerna är identiska när det gäller dimensioner och formtyp.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// Den första formen har inga effekter, och den andra har en skugga och en tjock kontur.
// Dessa effekter gör silhuettens storlek på den andra formen större än den första.
// Även om rektangelns storlek visas när vi klickar på dessa former i Microsoft Word,
// så påverkas de synliga yttre gränserna för den andra formen av skuggan och konturen och är därför större.
// Vi kan använda metoden \"AdjustWithEffects\" för att se den verkliga storleken på formen.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// Skapa ett RectangleF-objekt, som representerar en rektangel,
// som vi potentiellt kan använda som koordinater och gränser för en form.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// Kör den här metoden för att få rektangelns storlek justerad för alla våra formeffekter.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Eftersom formen inte har några kantförändrande effekter påverkas dess gränsdimensioner inte.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// Verifiera den slutgiltiga omfattningen av den första formen, i punkter.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Formeffekterna har förflyttat formens synliga övre vänstra hörn något.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// Effekterna har också påverkat formens synliga dimensioner.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// Effekterna har också påverkat formens synliga gränser.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
