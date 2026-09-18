---
title: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions-Methode"
linktitle: "CreateSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions-Methode. Erstellt ein SaveOptions-Objekt einer Klasse, die für das angegebene Speicherformat geeignet ist, in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


Erstellt ein Speicheroptionen-Objekt einer Klasse, die für das angegebene Speicherformat geeignet ist.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Das Speicherformat, für das ein SaveOptions-Objekt erstellt werden soll. |

### ReturnValue

Ein Objekt einer Klasse, die von [SaveOptions](../) abgeleitet ist.

## Siehe auch

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


Erstellt ein Speicheroptionen-Objekt einer Klasse, die für die Dateierweiterung geeignet ist, die im angegebenen Dateinamen angegeben ist.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Die Erweiterung dieses Dateinamens bestimmt die Klasse des zu erstellenden SaveOptions-Objekts. |

### ReturnValue

Ein Objekt einer Klasse, die von [SaveOptions](../) abgeleitet ist.

## Beispiele



Zeigt, wie man eine Standardvorlage für Dokumente festlegt, die keine angehängten Vorlagen haben.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aktivieren Sie die automatische Stilaktualisierung, aber hängen Sie kein Vorlagendokument an.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Da kein Vorlagendokument vorhanden ist, hatte das Dokument keinen Ort, um Stiländerungen nachzuverfolgen.
// Verwenden Sie ein SaveOptions-Objekt, um automatisch eine Vorlage festzulegen
// wenn ein Dokument, das wir speichern, keine hat.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## Siehe auch

* Class [SaveOptions](../)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
