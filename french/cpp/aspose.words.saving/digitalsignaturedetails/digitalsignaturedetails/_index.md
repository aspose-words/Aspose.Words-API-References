---
title: "Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails constructeur"
linktitle: "DigitalSignatureDetails"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails constructeur. Initialise une nouvelle instance de la classe DigitalSignatureDetails en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails::DigitalSignatureDetails constructor


Initialise une nouvelle instance de la classe [DigitalSignatureDetails](../).

```cpp
Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails(const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certificateHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| certificateHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | Un conteneur de certificat qui contient le certificat lui-même. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | Options de signature à utiliser pour signer un document. |

## Exemples



Montre comment signer un document OOXML.
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

## Voir aussi

* Class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* Class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
