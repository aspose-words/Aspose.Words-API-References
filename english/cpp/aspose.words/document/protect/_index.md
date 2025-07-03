---
title: Aspose::Words::Document::Protect method
linktitle: Protect
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::Protect method. Protects the document from changes without changing the existing password or assigns a random password in C++.'
type: docs
weight: 67000
url: /cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


Protects the document from changes without changing the existing password or assigns a random password.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| Parameter | Type | Description |
| --- | --- | --- |
| type | Aspose::Words::ProtectionType | Specifies the protection type for the document. |
## Remarks


When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

When you protect a document, and the document already has a protection password, the existing protection password is not changed.

When you protect a document, and the document does not have a protection password, this method assigns a random password that makes it impossible to unprotect the document in Microsoft Word, but you still can unprotect the document in Aspose.Words as it does not require a password when unprotecting.

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

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


Protects the document from changes and optionally sets a protection password.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| type | Aspose::Words::ProtectionType | Specifies the protection type for the document. |
| password | const System::String\& | The password to protect the document with. Specify **null** or empty string if you want to protect the document without a password. |
## Remarks


When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection. Write protection is specified using the [WriteProtection](../get_writeprotection/).

## Examples



Shows how to protect and unprotect a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// If we open this document with Microsoft Word intending to edit it,
// we will need to apply the password to get through the protection.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// Note that the protection only applies to Microsoft Word users opening our document.
// We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// There are two ways of removing protection from a document.
// 1 - With no password:
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - With the correct password:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## See Also

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
