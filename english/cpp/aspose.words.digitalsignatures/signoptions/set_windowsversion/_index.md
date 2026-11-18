---
title: Aspose::Words::DigitalSignatures::SignOptions::set_WindowsVersion method
linktitle: set_WindowsVersion
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::SignOptions::set_WindowsVersion method. Sets the Windows version for the digital signature. Default value is "6.1" in C++.'
type: docs
weight: 16667
url: /cpp/aspose.words.digitalsignatures/signoptions/set_windowsversion/
---
## SignOptions::set_WindowsVersion method


Sets the Windows version for the digital signature. Default value is "6.1".

```cpp
void Aspose::Words::DigitalSignatures::SignOptions::set_WindowsVersion(const System::String & value)
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
ASSERT_EQ(signedDoc->get_DigitalSignatures()->get_Count(), 1);
ASSERT_TRUE(signature->get_IsValid());
ASSERT_EQ(signature->get_WindowsVersion(), u"10.0");
ASSERT_EQ(signature->get_ApplicationVersion(), u"16.0.19127");
ASSERT_EQ(signature->get_OfficeVersion(), u"16.0.19127/27");
ASSERT_EQ(signature->get_HorizontalResolution(), 1024);
ASSERT_EQ(signature->get_VerticalResolution(), 768);
ASSERT_EQ(signature->get_ColorDepth(), 24);
```
## See Also

* [get_WindowsVersion](../get_windowsversion/)

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
