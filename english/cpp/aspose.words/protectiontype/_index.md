---
title: Aspose::Words::ProtectionType enum
linktitle: ProtectionType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ProtectionType enum. Protection type for a document in C++.'
type: docs
weight: 111000
url: /cpp/aspose.words/protectiontype/
---
## ProtectionType enum


Protection type for a document.

```cpp
enum class ProtectionType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AllowOnlyComments | 1 | User can only modify comments in the document. |
| AllowOnlyFormFields | 2 | User can only enter data in the form fields in the document. |
| AllowOnlyRevisions | 0 | User can only add revision marks to the document. |
| ReadOnly | 3 | No changes are allowed to the document. Available since Microsoft Word 2003. |
| NoProtection | -1 | The document is not protected. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
