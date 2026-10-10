---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter method"
linktitle: "MoveToHeaderFooter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter method. Flyttar markören till början av ett sidhuvud eller en sidfot i det aktuella avsnittet i C++."
type: docs
weight: 57000
url: /sv/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


Flyttar markören till början av ett sidhuvud eller sidfot i den aktuella sektionen.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Anger vilket sidhuvud eller vilken sidfot som ska flyttas till. |
## Anmärkningar


Efter att du har flyttat markören till ett sidhuvud eller en sidfot kan du använda resten av [DocumentBuilder](../)-metoderna för att ändra innehållet i sidhuvudet eller sidfoten.

Om du vill skapa olika sidhuvuden och sidfötter för första sidan måste du ställa in [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/).

Om du vill skapa olika sidhuvuden och sidfötter för jämna och udda sidor, måste du ställa in [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/).

Använd [MoveToSection()](../movetosection/) för att gå ut från sidhuvudet till huvudtexten.

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

## Se även

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
