---
title: "Aspose::Words::Drawing::ShapeBase::get_Top metod"
linktitle: "get_Top"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Top metod. Hämtar eller anger positionen för den övre kanten av den omgivande blocket för formen i C++."
type: docs
weight: 52000
url: /sv/cpp/aspose.words.drawing/shapebase/get_top/
---
## ShapeBase::get_Top method


Hämtar eller anger positionen för den övre kanten av formens omgivande block.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Top()
```

## Anmärkningar


För en toppnivåform är värdet i punkter och relativt till formens ankare.

För former i en grupp är värdet i koordinatrymden och enheterna för den överordnade gruppen.

Standardvärdet är 0.

Har endast effekt för flytande former.

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

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
