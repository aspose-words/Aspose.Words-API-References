---
title: "Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat metod"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat metod. Anger formatet som dokumentet kommer att sparas i om detta sparalternativobjekt används. Kan vara Odt eller Ott i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/odtsaveoptions/get_saveformat/
---
## OdtSaveOptions::get_SaveFormat method


Anger formatet som dokumentet kommer att sparas i om detta sparalternativobjekt används. Kan vara [Odt](../../../aspose.words/saveformat/) eller [Ott](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat() override
```


## Exempel



Visar hur man krypterar ett sparat ODT/OTT‑dokument med ett lösenord och sedan laddar det med Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Skapa en ny OdtSaveOptions och skicka antingen "SaveFormat.Odt",
// eller "SaveFormat.Ott" som format för att spara dokumentet i.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Om vi öppnar detta dokument med en lämplig redigerare,
// kommer den att be oss om lösenordet vi angav i SaveOptions‑objektet.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Om vi vill öppna eller redigera detta dokument igen med Aspose.Words,
// måste vi tillhandahålla ett LoadOptions‑objekt med rätt lösenord till laddningskonstruktorn.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Se även

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
