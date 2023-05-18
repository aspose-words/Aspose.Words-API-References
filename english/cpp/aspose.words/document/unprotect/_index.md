---
title: Aspose::Words::Document::Unprotect method
linktitle: Unprotect
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::Unprotect method. Removes protection from the document regardless of the password in C++.'
type: docs
weight: 95000
url: /cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


Removes protection from the document regardless of the password.

```cpp
void Aspose::Words::Document::Unprotect()
```

## Remarks


This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection. Write protection is specified using the [WriteProtection](../get_writeprotection/).

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


Removes protection from the document if a correct password is specified.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| password | const System::String\& | The password to unprotect the document with. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## Remarks


This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection. Write protection is specified using the [WriteProtection](../get_writeprotection/).

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
