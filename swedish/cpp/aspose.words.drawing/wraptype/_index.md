---
title: "Aspose::Words::Drawing::WrapType-enum"
linktitle: "WrapType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::WrapType enum. Anger hur text omsluts runt en form eller bild i C++."
type: docs
weight: 45000
url: /sv/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


Anger hur text omsluter en form eller bild.

```cpp
enum class WrapType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 3 | Ingen textomslag runt formen. Formen placeras bakom eller framför texten. |
| Inbäddad | 0 | Formen förblir på samma lager som texten och behandlas som ett tecken. |
| TopBottom | 1 | Texten stannar vid formens övre kant och fortsätter på raden under formen. |
| Square | 2 | Omsluter texten runt alla sidor av formens fyrkantiga omgivningsruta. |
| Tight | 4 | Omsluter tätt runt formens kanter, istället för att omsluta omgivningsrutan. |
| Through | 5 | Samma som Tight, men omsluter även de öppna delarna av formen. |


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
