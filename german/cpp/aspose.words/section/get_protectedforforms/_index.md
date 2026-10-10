---
title: "Aspose::Words::Section::get_ProtectedForForms Methode"
linktitle: "get_ProtectedForForms"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::get_ProtectedForForms Methode. Wahr, wenn der Abschnitt für Formulare geschützt ist. Wenn ein Abschnitt für Formulare geschützt ist, können Benutzer in Microsoft Word in C++ nur Text in Formularfeldern auswählen und ändern."
type: docs
weight: 14000
url: /de/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


True, wenn der Abschnitt für Formulare geschützt ist. Wenn ein Abschnitt für Formulare geschützt ist, können Benutzer in Microsoft Word nur Text in Formularfeldern auswählen und ändern.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


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

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
