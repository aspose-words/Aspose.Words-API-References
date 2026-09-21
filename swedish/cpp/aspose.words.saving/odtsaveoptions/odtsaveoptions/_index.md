---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions konstruktor"
linktitle: "OdtSaveOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions konstruktor. Initierar en ny instans av denna klass som kan användas för att spara ett dokument i Odt‑format i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


Initierar en ny instans av denna klass som kan användas för att spara ett dokument i [Odt](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## Exempel



Visar hur man får ett sparat dokument att följa ett äldre ODT-schema.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Se även

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


Initierar en ny instans av denna klass som kan användas för att spara ett dokument i [Odt](../../../aspose.words/saveformat/) eller [Ott](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Kan vara [Odt](../../../aspose.words/saveformat/) eller [Ott](../../../aspose.words/saveformat/). |

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
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Initierar en ny instans av denna klass som kan användas för att spara ett dokument i [Odt](../../../aspose.words/saveformat/) format krypterat med ett lösenord.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## Se även

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
