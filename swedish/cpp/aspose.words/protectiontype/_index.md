---
title: "Aspose::Words::ProtectionType enum"
linktitle: "ProtectionType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ProtectionType enum. Skyddstyp för ett dokument i C++."
type: docs
weight: 111000
url: /sv/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


Skyddstyp för ett dokument.

```cpp
enum class ProtectionType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| AllowOnlyComments | 1 | Användaren kan endast ändra kommentarer i dokumentet. |
| AllowOnlyFormFields | 2 | Användaren kan endast ange data i formulärfälten i dokumentet. |
| AllowOnlyRevisions | 0 | Användaren kan endast lägga till revisionsmarkeringar i dokumentet. |
| ReadOnly | 3 | Inga ändringar är tillåtna i dokumentet. Tillgänglig sedan Microsoft Word 2003. |
| NoProtection | -1 | Dokumentet är inte skyddat. |


## Exempel



Visar hur man stänger av skydd för ett avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Applicera skrivskydd på varje avsnitt i dokumentet.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Stäng av skrivskydd för det första avsnittet.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// I detta utdata-dokument kommer vi att kunna redigera det första avsnittet fritt,
// och vi kommer endast att kunna redigera innehållet i formulärfältet i det andra avsnittet.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
