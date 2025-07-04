---
title: Aspose::Words::FileFormatInfo class
linktitle: FileFormatInfo
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatInfo class. Contains data returned by FileFormatUtil document format detection methods. To learn more, visit the  documentation article in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


Contains data returned by [FileFormatUtil](../fileformatutil/) document format detection methods. To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/) documentation article.

```cpp
class FileFormatInfo : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | Gets the detected encoding if applicable to the current document format. At the moment detects encoding only for HTML documents. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | Returns **true** if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not specify whether the signature is valid or not. |
| [get_HasMacros](./get_hasmacros/)() const | Returns **true** if this document contains a VBA macros. |
| [get_IsEncrypted](./get_isencrypted/)() const | Returns **true** if the document is encrypted and requires a password to open. |
| [get_LoadFormat](./get_loadformat/)() const | Gets the detected document format. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarks


You do not create instances of this class directly. Objects of this class are returned by [DetectFileFormat()](../) methods.

## Examples



Shows how to use the [FileFormatUtil](../fileformatutil/) class to detect the document format and encryption. 
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


Shows how to use the [FileFormatUtil](../fileformatutil/) class to detect the document format and presence of digital signatures. 
```cpp
// Use a FileFormatInfo instance to verify that a document is not digitally signed.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Use a new FileFormatInstance to confirm that it is signed.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// We can load and access the signatures of a signed document in a collection like this.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
