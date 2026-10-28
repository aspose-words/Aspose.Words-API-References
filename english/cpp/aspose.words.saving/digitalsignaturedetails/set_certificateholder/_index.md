---
title: Aspose::Words::Saving::DigitalSignatureDetails::set_CertificateHolder method
linktitle: set_CertificateHolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DigitalSignatureDetails::set_CertificateHolder method. Sets a CertificateHolder object that contains the certificate used to sign a document in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.saving/digitalsignaturedetails/set_certificateholder/
---
## DigitalSignatureDetails::set_CertificateHolder method


Sets a [CertificateHolder](../get_certificateholder/) object that contains the certificate used to sign a document.

```cpp
void Aspose::Words::Saving::DigitalSignatureDetails::set_CertificateHolder(const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> & value)
```

## Examples


Shows how to sign OOXML document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Some comments");
signOptions->set_SignTime(System::DateTime::get_Now());
auto digitalSignatureDetails = System::MakeObject<Aspose::Words::Saving::DigitalSignatureDetails>(certificateHolder, signOptions);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_DigitalSignatureDetails(digitalSignatureDetails);

ASPOSE_ASSERT_EQ(certificateHolder, digitalSignatureDetails->get_CertificateHolder());
ASSERT_EQ(u"Some comments", digitalSignatureDetails->get_SignOptions()->get_Comments());

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
```
## See Also

* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
