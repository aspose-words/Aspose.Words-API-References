---
title: "Aspose::Words::Section::get_ProtectedForForms metod"
linktitle: "get_ProtectedForForms"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Section::get_ProtectedForForms metod. Sant om avsnittet är skyddat för formulär. När ett avsnitt är skyddat för formulär kan användare endast markera och ändra text i formulärfält i Microsoft Word i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


Sant om avsnittet är skyddat för formulär. När ett avsnitt är skyddat för formulär kan användare endast markera och ändra text i formulärfält i Microsoft Word.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


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

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
