---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty metod"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty metod. Hämtar eller anger ett värde som bestämmer om LastPrinted‑egenskapen uppdateras innan sparning i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


Hämtar eller anger ett värde som bestämmer om egenskapen [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) uppdateras innan sparning.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## Exempel



Visar hur man uppdaterar ett dokuments "Last printed"-egenskap när man sparar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// Denna flagga bestämmer om datumet för senaste utskrift, som är en inbyggd egenskap, uppdateras.
// Om så är fallet, då datumet för dokumentets senaste sparoperation
// med detta SaveOptions-objekt som skickas som parameter används som utskriftsdatum.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// I Microsoft Word 2003 kan den här egenskapen hittas via Arkiv -> Egenskaper -> Statistik -> Utskriven.
// Den kan också visas i dokumentets brödtext genom att använda ett PRINTDATE-fält.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Öppna det sparade dokumentet och verifiera sedan värdet på egenskapen.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```

## Se även

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
