---
title: "Aspose::Words::PageSetup::get_PageHeight metod"
linktitle: "get_PageHeight"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_PageHeight metod. Returnerar eller anger sidans höjd i punkter i C++."
type: docs
weight: 33000
url: /sv/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


Returnerar eller anger sidans höjd i punkter.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
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

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
