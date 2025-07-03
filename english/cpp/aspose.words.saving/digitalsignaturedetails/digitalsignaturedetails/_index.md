---
title: Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails constructor
linktitle: DigitalSignatureDetails
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails constructor. Initializes a new instance of DigitalSignatureDetails class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails::DigitalSignatureDetails constructor


Initializes a new instance of [DigitalSignatureDetails](../) class.

```cpp
Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails(const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certificateHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| certificateHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | A certificate holder which contains the certificate itself. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | Signature options to use for signing a document. |

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

* Class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* Class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
