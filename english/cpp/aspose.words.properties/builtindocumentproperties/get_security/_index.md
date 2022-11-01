---
title: get_Security
second_title: Aspose.Words for C++ API Reference
description: Specifies the security level of a document as a numeric value.
type: docs
weight: 300
url: /cpp/aspose.words.properties/builtindocumentproperties/get_security/
---
## BuiltInDocumentProperties.get_Security method


Specifies the security level of a document as a numeric value.

```cpp
Aspose::Words::Properties::DocumentSecurity Aspose::Words::Properties::BuiltInDocumentProperties::get_Security()
```


Use this property for informational purposes only because Microsoft Word does not always set this property. This property is available in DOC and OOXML documents only.

To protect or unprotect a document use the **Protect()** and [Unprotect](../../../aspose.words/document/unprotect/) methods.

Aspose.Words updates this property to a correct value before saving a document.

## Examples




Shows how to use document properties to display the security level of a document. 
```cpp
auto doc = MakeObject<Document>();

ASSERT_EQ(DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// If we configure a document to be read-only, it will display this status using the "Security" built-in property.
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(ArtifactsDir + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(
    DocumentSecurity::ReadOnlyRecommended,
    MakeObject<Document>(ArtifactsDir + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Write-protect a document, and then verify its security level.
doc = MakeObject<Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(ArtifactsDir + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(DocumentSecurity::ReadOnlyEnforced,
          MakeObject<Document>(ArtifactsDir + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" is a descriptive property. We can edit its value manually.
doc = MakeObject<Document>();

doc->Protect(ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(ArtifactsDir + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(DocumentSecurity::ReadOnlyExceptAnnotations,
          MakeObject<Document>(ArtifactsDir + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")
              ->get_BuiltInDocumentProperties()
              ->get_Security());
```

