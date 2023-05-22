---
title: Aspose::Words::Settings::WriteProtection::get_IsWriteProtected method
linktitle: get_IsWriteProtected
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::WriteProtection::get_IsWriteProtected method. Returns true when a write protection password is set in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.settings/writeprotection/get_iswriteprotected/
---
## WriteProtection::get_IsWriteProtected method


Returns **true** when a write protection password is set.

```cpp
bool Aspose::Words::Settings::WriteProtection::get_IsWriteProtected()
```


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

## See Also

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
