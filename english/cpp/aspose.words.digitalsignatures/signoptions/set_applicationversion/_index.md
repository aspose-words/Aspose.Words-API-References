---
title: Aspose::Words::DigitalSignatures::SignOptions::set_ApplicationVersion method
linktitle: set_ApplicationVersion
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::SignOptions::set_ApplicationVersion method. Sets the application version for the digital signature. Default value is "12.0" in C++.'
type: docs
weight: 10334
url: /cpp/aspose.words.digitalsignatures/signoptions/set_applicationversion/
---
## SignOptions::set_ApplicationVersion method


Sets the application version for the digital signature. Default value is "12.0".

```cpp
void Aspose::Words::DigitalSignatures::SignOptions::set_ApplicationVersion(const System::String & value)
```

## Examples


Shows how to sign a document with additional signing options.

```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_WindowsVersion(u"10.0");
signOptions->set_ApplicationVersion(u"16.0.19127");
signOptions->set_OfficeVersion(u"16.0.19127/27");
signOptions->set_HorizontalResolution(1024);
signOptions->set_VerticalResolution(768);
signOptions->set_ColorDepth(24);

System::ArrayPtr<uint8_t> certBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"morzal.pfx");
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = CertificateHolder::Create(certBytes, u"aw");
DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"DigitalSignatureUtil.docx"));

System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature> signature = signedDoc->get_DigitalSignatures()->idx_get(0);
ASSERT_EQ(1, signedDoc->get_DigitalSignatures()->get_Count());
ASSERT_TRUE(signature->get_IsValid());
ASSERT_EQ(u"10.0", signature->get_WindowsVersion());
ASSERT_EQ(u"16.0.19127", signature->get_ApplicationVersion());
ASSERT_EQ(u"16.0.19127/27", signature->get_OfficeVersion());
ASSERT_EQ(1024, signature->get_HorizontalResolution());
ASSERT_EQ(768, signature->get_VerticalResolution());
ASSERT_EQ(24, signature->get_ColorDepth());
```
## See Also

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
