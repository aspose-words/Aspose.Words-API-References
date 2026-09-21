---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty metod"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty metod. Hämtar eller anger ett värde som bestämmer om egenskapen LastSavedTime uppdateras före sparning i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


Hämtar eller anger ett värde som bestämmer om egenskapen [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) uppdateras före sparning.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## Exempel



Visar hur man avgör om dokumentets "Last saved time"-egenskap ska bevaras vid sparande.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions‑objekt.
// och sedan skicka den till dokumentets sparningsmetod för att ändra hur vi sparar dokumentet.
// Ställ in egenskapen "UpdateLastSavedTimeProperty" till "true" för att
// sätt den utgående dokumentets "Last saved time" inbyggda egenskap till aktuellt datum/tid.
// Ställ in egenskapen "UpdateLastSavedTimeProperty" till "false" för att
// bevara det ursprungliga värdet på den inmatade dokumentets "Last saved time" inbyggda egenskap.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx");
System::DateTime lastSavedTimeNew = doc->get_BuiltInDocumentProperties()->get_LastSavedTime();

if (updateLastSavedTimeProperty)
{
    ASSERT_TRUE((System::DateTime::get_Now() - lastSavedTimeNew).get_Days() < 1);
}
else
{
    ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), lastSavedTimeNew);
}
```

## Se även

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
