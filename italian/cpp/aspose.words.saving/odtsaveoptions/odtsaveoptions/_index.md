---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions costruttore"
linktitle: "OdtSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions costruttore. Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nel formato Odt in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nel formato [Odt](../../../aspose.words/saveformat/) .

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## Esempi



Mostra come far conformare un documento salvato a uno schema ODT più vecchio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Vedi anche

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nel formato [Odt](../../../aspose.words/saveformat/) o [Ott](../../../aspose.words/saveformat/) .

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Può essere [Odt](../../../aspose.words/saveformat/) o [Ott](../../../aspose.words/saveformat/). |

## Esempi



Mostra come crittografare un documento ODT/OTT salvato con una password, e poi caricarlo usando Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Crea un nuovo OdtSaveOptions, e passa "SaveFormat.Odt",
// o "SaveFormat.Ott" come formato per salvare il documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Se apriamo questo documento con un editor appropriato,
// ti chiederà la password che abbiamo specificato nell'oggetto SaveOptions.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Se desideriamo aprire o modificare nuovamente questo documento usando Aspose.Words,
// dovremo fornire un oggetto LoadOptions con la password corretta al costruttore di caricamento.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Inizializza una nuova istanza di questa classe che può essere usata per salvare un documento nel formato [Odt](../../../aspose.words/saveformat/) cifrato con una password.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## Vedi anche

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
