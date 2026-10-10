---
title: "Aspose::Words::ProtectionType Enum"
linktitle: "ProtectionType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ProtectionType Enum. Schutztyp für ein Dokument in C++."
type: docs
weight: 111000
url: /de/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


Schutztyp für ein Dokument.

```cpp
enum class ProtectionType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AllowOnlyComments | 1 | Benutzer kann im Dokument nur Kommentare ändern. |
| AllowOnlyFormFields | 2 | Benutzer kann im Dokument nur Daten in Formularfelder eingeben. |
| AllowOnlyRevisions | 0 | Benutzer kann im Dokument nur Revisionsmarken hinzufügen. |
| ReadOnly | 3 | Keine Änderungen am Dokument erlaubt. Verfügbar seit Microsoft Word 2003. |
| NoProtection | -1 | Das Dokument ist nicht geschützt. |


## Beispiele



Zeigt, wie man den Schutz für einen Abschnitt deaktiviert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Wenden Sie Schreibschutz auf jeden Abschnitt im Dokument an.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Deaktivieren Sie den Schreibschutz für den ersten Abschnitt.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// In diesem Ausgabedokument können wir den ersten Abschnitt frei bearbeiten,
// und wir können nur den Inhalt des Formularfelds im zweiten Abschnitt bearbeiten.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
