---
title: Aspose::Words::Section::get_ProtectedForForms method
linktitle: get_ProtectedForForms
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Section::get_ProtectedForForms method. True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


## Examples



Shows how to turn off protection for a section. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Apply write protection to every section in the document.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Turn off write protection for the first section.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// In this output document, we will be able to edit the first section freely,
// and we will only be able to edit the contents of the form field in the second section.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## See Also

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
