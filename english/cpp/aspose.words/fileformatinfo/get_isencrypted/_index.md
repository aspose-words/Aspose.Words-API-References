---
title: Aspose::Words::FileFormatInfo::get_IsEncrypted method
linktitle: get_IsEncrypted
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatInfo::get_IsEncrypted method. Returns true if the document is encrypted and requires a password to open in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


Returns **true** if the document is encrypted and requires a password to open.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## Remarks


This property exists to help you sort documents that are encrypted from those that are not. If you attempt to load an encrypted document using Aspose.Words without supplying a password an exception will be thrown. You can use this property to detect whether a document requires a password and take some action before loading a document, for example, prompt the user for a password.

## Examples



Shows how to use the [FileFormatUtil](../../fileformatutil/) class to detect the document format and encryption. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configure a SaveOptions object to encrypt the document
// with a password when we save it, and then save the document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Verify the file type of our document, and its encryption status.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```

## See Also

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
