---
title: get_HasDigitalSignature
second_title: Aspose.Words for C++ API Reference
description: Returns true if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not specify whether the signature is valid or not.
type: docs
weight: 14
url: /cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo.get_HasDigitalSignature method


Returns true if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not specify whether the signature is valid or not.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```


This property exists to help you sort documents that are digitally signed from those that are not. If you use Aspose.Words to modify and save a document that is digitally signed, then the digital signature will be lost. This is by design because a digital signature exists to guard the authenticity of a document. Using this property you can detect digitally signed documents before processing them in the same way as normal documents and take some action to avoid losing the digital signature, for example notify the user.

## Examples




Shows how to use the [FileFormatUtil](../../fileformatutil/) class to detect the document format and presence of digital signatures. 
```cpp
// Use a FileFormatInfo instance to verify that a document is not digitally signed.
SharedPtr<FileFormatInfo> info = FileFormatUtil::DetectFileFormat(MyDir + u"Document.docx");

ASSERT_EQ(u".docx", FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw", nullptr);
auto signOptions = MakeObject<SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
DigitalSignatureUtil::Sign(MyDir + u"Document.docx", ArtifactsDir + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Use a new FileFormatInstance to confirm that it is signed.
info = FileFormatUtil::DetectFileFormat(ArtifactsDir + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// We can load and access the signatures of a signed document in a collection like this.
ASSERT_EQ(1, DigitalSignatureUtil::LoadSignatures(ArtifactsDir + u"File.DetectDigitalSignatures.docx")->get_Count());
```

