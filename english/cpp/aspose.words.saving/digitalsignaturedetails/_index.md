---
title: Aspose::Words::Saving::DigitalSignatureDetails class
linktitle: DigitalSignatureDetails
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DigitalSignatureDetails class. Contains details for signing a document with a digital signature in C++.'
type: docs
weight: 2500
url: /cpp/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class


Contains details for signing a document with a digital signature.

```cpp
class DigitalSignatureDetails : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [DigitalSignatureDetails](./digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Initializes a new instance of [DigitalSignatureDetails](./) class. |
| [get_CertificateHolder](./get_certificateholder/)() const | Gets or sets a [CertificateHolder](./get_certificateholder/) object that contains the certificate used to sign a document. |
| [get_SignOptions](./get_signoptions/)() const | Gets or sets a [SignOptions](./get_signoptions/) object used to sign a document. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Setter for [Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder](./get_certificateholder/). |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Setter for [Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions](./get_signoptions/). |
| static [Type](./type/)() |  |

## Examples



Shows how to sign OOXML document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
