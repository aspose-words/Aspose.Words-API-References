---
title: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType metod"
linktitle: "get_ContentType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType metod. Returnerar Content-Type-strängen (Internet Media Type) som identifierar typen av det sparade dokumentet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


Returnerar Content-Type-strängen (Internet Media Type) som identifierar typen av det sparade dokumentet.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## Exempel



Visar hur man får åtkomst till utdata parametrar för ett dokuments sparningsoperation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Efter att vi har sparat ett dokument kan vi komma åt Internet Media Type (MIME-typ) för det nyss skapade utdata-dokumentet.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Denna egenskap förändras beroende på sparformatet.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## Se även

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
