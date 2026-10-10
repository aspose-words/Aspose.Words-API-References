---
title: "Aspose::Words::PageSetup::get_PageWidth metod"
linktitle: "get_PageWidth"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_PageWidth metod. Returnerar eller anger bredden på sidan i punkter i C++."
type: docs
weight: 36000
url: /sv/cpp/aspose.words/pagesetup/get_pagewidth/
---
## PageSetup::get_PageWidth method


Returnerar eller anger sidans bredd i punkter.

```cpp
double Aspose::Words::PageSetup::get_PageWidth()
```


## Exempel



Visar hur man infogar en bild och använder den som vattenstämpel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga bilden i sidhuvudet så att den syns på varje sida.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Placera bilden i sidans centrum.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
