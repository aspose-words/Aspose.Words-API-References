---
title: Aspose::Words::Properties::DocumentSecurity enum
linktitle: DocumentSecurity
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentSecurity enum. Used as a value for the Security property. Specifies the security level of a document as a numeric value in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


Used as a value for the [Security](../builtindocumentproperties/get_security/) property. Specifies the security level of a document as a numeric value.

```cpp
enum class DocumentSecurity
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | There are no security states specified by the property. |
| PasswordProtected | 1 | The document is password protected. (Note has never been seen in a document so far). |
| ReadOnlyRecommended | 2 | The document to be opened read-only if possible, but the setting can be overridden. |
| ReadOnlyEnforced | 4 | The document to always be opened read-only. |
| ReadOnlyExceptAnnotations | 8 | The document to always be opened read-only except for annotations. |


## Examples



Shows how to use document properties to display the security level of a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// If we configure a document to be read-only, it will display this status using the "Security" built-in property.
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Write-protect a document, and then verify its security level.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" is a descriptive property. We can edit its value manually.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## See Also

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
