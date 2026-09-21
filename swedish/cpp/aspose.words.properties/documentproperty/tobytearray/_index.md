---
title: "Aspose::Words::Properties::DocumentProperty::ToByteArray metod"
linktitle: "ToByteArray"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentProperty::ToByteArray metod. Returnerar egenskapens värde som byte‑array i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


Returnerar egenskapsvärdet som byte-array.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## Anmärkningar


Kastar ett undantag om egenskapstypen inte är [ByteArray](../../propertytype/).

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
