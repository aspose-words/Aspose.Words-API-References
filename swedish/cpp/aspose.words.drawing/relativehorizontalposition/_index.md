---
title: "Aspose::Words::Drawing::RelativeHorizontalPosition enum"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::RelativeHorizontalPosition enum. Anger i förhållande till vad den horisontella positionen för en form eller textram är i C++."
type: docs
weight: 33000
url: /sv/cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


Anger relativt vad den horisontella positionen för en form eller textruta är.

```cpp
enum class RelativeHorizontalPosition
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Marginal | 0 | Anger att den horisontella positioneringen ska vara relativ till sidans marginaler. |
| Page | 1 | Objektet är placerat relativt till sidans vänstra kant. |
| Kolumn | 2 | Objektet är placerat relativt till kolumnens vänstra sida. |
| Character | 3 | Objektet är placerat relativt till styckets vänstra sida. |
| LeftMargin | 4 | Anger att den horisontella positioneringen ska vara relativ till sidans vänstra marginal. |
| RightMargin | 5 | Anger att den horisontella positioneringen ska vara relativ till sidans högra marginal. |
| InsideMargin | 6 | Anger att den horisontella positioneringen ska vara relativ till den inre marginalen på den aktuella sidan (vänster marginal på udda sidor, högre på jämna sidor). |
| OutsideMargin | 7 | Anger att den horisontella positioneringen ska vara relativ till den yttre marginalen på den aktuella sidan (högra marginalen på udda sidor, vänstra på jämna sidor). |
| Default | n/a | Standardvärdet är [Column](./). |


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


Visar hur man infogar en flytande bild i sidans centrum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den till sidans centrum.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
