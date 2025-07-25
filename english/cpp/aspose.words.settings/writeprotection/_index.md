---
title: Aspose::Words::Settings::WriteProtection class
linktitle: WriteProtection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::WriteProtection class. Specifies write protection settings for a document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


Specifies write protection settings for a document. To learn more, visit the [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/) documentation article.

```cpp
class WriteProtection : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | Returns **true** when a write protection password is set. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | Specifies whether the document author has recommended that the document be opened as read-only. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | Setter for [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | Sets the write protection password for the document. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | Returns **true** if the specified password is the same as the write-protection password the document was protected with. If document is not write-protected with password then returns **false**. |
## Remarks


Write protection specifies whether the author has recommended that the document is to be opened as read-only and/or require a password to modify a document.

Write protection is different from document protection. Write protection is specified in Microsoft Word in the options of the Save As dialog box.

You do not create instances of this class directly. You access document protection settings via the [WriteProtection](../../aspose.words/document/get_writeprotection/) property.

## Examples



Shows how to protect a document with a password. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Enter a password up to 15 characters in length, and then verify the document's protection status.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## See Also

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
