---
title: "Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions méthode"
linktitle: "get_SignOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions méthode. Obtient ou définit un objet SignOptions utilisé pour signer un document en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/digitalsignaturedetails/get_signoptions/
---
## DigitalSignatureDetails::get_SignOptions method


Obtient ou définit un objet [SignOptions](./) utilisé pour signer un document.

```cpp
const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> & Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions() const
```


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

* Class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
