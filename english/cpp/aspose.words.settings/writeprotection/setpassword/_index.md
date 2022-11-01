---
title: SetPassword
second_title: Aspose.Words for C++ API Reference
description: Sets the write protection password for the document.
type: docs
weight: 40
url: /cpp/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection.SetPassword method


Sets the write protection password for the document.

```cpp
void Aspose::Words::Settings::WriteProtection::SetPassword(const System::String &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| password | const System::String\& | The password to set. Cannot be null, but can be an empty string. |

If a password is set, Microsoft Word will require the user to enter it or open the document as read-only.

## Examples




Shows how to protect a document with a password. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Enter a password up to 15 characters in length, and then verify the document's protection status.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
doc->Save(ArtifactsDir + u"Document.WriteProtection.docx");
doc = MakeObject<Document>(ArtifactsDir + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = MakeObject<DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

