---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty metod"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty metod. Hämtar eller anger ett värde som bestämmer om egenskapen CreatedTime uppdateras innan sparning. Standardvärdet är false; i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


Hämtar eller anger ett värde som bestämmer om egenskapen [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) uppdateras innan sparning. Standardvärdet är **false**;.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## Exempel



Visar hur man uppdaterar ett dokuments "CreatedTime"‑egenskap vid sparning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// Denna flagga bestämmer om den skapade tiden, som är en inbyggd egenskap, uppdateras.
// Om så är fallet, då datumet för dokumentets senaste sparoperation
// med detta SaveOptions-objekt som skickas som en parameter används som den skapade tiden.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Öppna det sparade dokumentet och verifiera sedan värdet på egenskapen.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## Se även

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
