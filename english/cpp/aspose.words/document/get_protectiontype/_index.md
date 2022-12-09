---
title: get_ProtectionType
second_title: Aspose.Words for C++ API Reference
description: Gets the currently active document protection type.
type: docs
weight: 534
url: /cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


Gets the currently active document protection type.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## Remarks


This property allows to retrieve the currently set document protection type. To change the document protection type use the [Protect()](../) and [Unprotect](../unprotect/) methods.

When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection. Write protection is specified using the [WriteProtection](../get_writeprotection/)

## Examples



Shows how to protect and unprotect a document. 
```cpp
auto doc = MakeObject<Document>();
doc->Protect(ProtectionType::ReadOnly, u"password");

ASSERT_EQ(ProtectionType::ReadOnly, doc->get_ProtectionType());

// If we open this document with Microsoft Word intending to edit it,
// we will need to apply the password to get through the protection.
doc->Save(ArtifactsDir + u"Document.Protect.docx");

// Note that the protection only applies to Microsoft Word users opening our document.
// We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
auto protectedDoc = MakeObject<Document>(ArtifactsDir + u"Document.Protect.docx");

ASSERT_EQ(ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = MakeObject<DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// There are two ways of removing protection from a document.
// 1 - With no password:
doc->Unprotect();

ASSERT_EQ(ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - With the correct password:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(ProtectionType::NoProtection, doc->get_ProtectionType());
```

## See Also

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
