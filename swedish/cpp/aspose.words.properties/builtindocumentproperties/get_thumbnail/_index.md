---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail metod"
linktitle: "get_Thumbnail"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail metod. Hämtar eller anger miniatyren för dokumentet i C++."
type: docs
weight: 28000
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


Hämtar eller anger miniatyrbilden för dokumentet.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## Anmärkningar


För närvarande används den här egenskapen endast när ett dokument exporteras till ePub, den läses inte från och skrivs inte till andra dokumentformat.

Bild i godtyckligt format kan tilldelas denna egenskap, men formatet kontrolleras vid export.

Endast gif-, jpeg- och png-bilder kan användas för ePub-publicering.

## Exempel



Visar hur man lägger till en miniatyr i ett dokument som vi sparar som en Epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Om vi sparar ett dokument, vars "Thumbnail"-egenskap innehåller bilddata som vi har lagt till, som en Epub,
// kan en läsare som öppnar det dokumentet visa bilden före den första sidan.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// Vi kan extrahera ett dokuments miniatyrbild och spara den till det lokala filsystemet.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## Se även

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
