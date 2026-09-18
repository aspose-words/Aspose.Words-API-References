---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions Konstruktor"
linktitle: "OdtSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions Konstruktor. Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im Odt-Format in C++ zu speichern."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [Odt](../../../aspose.words/saveformat/) Format zu speichern.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## Beispiele



Zeigt, wie ein gespeichertes Dokument an ein älteres ODT-Schema angepasst wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Siehe auch

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [Odt](../../../aspose.words/saveformat/) oder [Ott](../../../aspose.words/saveformat/) Format zu speichern.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Kann [Odt](../../../aspose.words/saveformat/) oder [Ott](../../../aspose.words/saveformat/) sein. |

## Beispiele



Zeigt, wie man ein gespeichertes ODT/OTT-Dokument mit einem Passwort verschlüsselt und es dann mit Aspose.Words lädt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Erstellen Sie ein neues OdtSaveOptions und übergeben Sie entweder \"SaveFormat.Odt\",
// oder \"SaveFormat.Ott\" als das Format, in dem das Dokument gespeichert werden soll.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Wenn wir dieses Dokument mit einem geeigneten Editor öffnen,
// wird es uns nach dem Passwort fragen, das wir im SaveOptions-Objekt angegeben haben.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Wenn wir dieses Dokument erneut mit Aspose.Words öffnen oder bearbeiten möchten,
// müssen wir dem Lade‑Konstruktor ein LoadOptions-Objekt mit dem korrekten Passwort übergeben.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [Odt](../../../aspose.words/saveformat/) Format mit einem Passwort verschlüsselt zu speichern.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## Siehe auch

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
