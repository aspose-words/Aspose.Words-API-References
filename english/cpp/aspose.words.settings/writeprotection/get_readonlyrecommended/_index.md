---
title: get_ReadOnlyRecommended
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the document author has recommended that the document be opened as read-only.
type: docs
weight: 14
url: /cpp/aspose.words.settings/writeprotection/get_readonlyrecommended/
---
## WriteProtection.get_ReadOnlyRecommended method


Specifies whether the document author has recommended that the document be opened as read-only.

```cpp
bool Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended() const
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

