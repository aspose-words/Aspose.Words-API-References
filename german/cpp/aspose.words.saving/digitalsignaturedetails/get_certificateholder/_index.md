---
title: "Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder Methode"
linktitle: "get_CertificateHolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder Methode. Liest oder setzt ein CertificateHolder-Objekt, das das zum Signieren eines Dokuments in C++ verwendete Zertifikat enthält."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/digitalsignaturedetails/get_certificateholder/
---
## DigitalSignatureDetails::get_CertificateHolder method


Liest oder setzt ein [CertificateHolder](./)-Objekt, das das zum Signieren eines Dokuments verwendete Zertifikat enthält.

```cpp
const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> & Aspose::Words::Saving::DigitalSignatureDetails::get_CertificateHolder() const
```


## Beispiele



Zeigt, wie man ein OOXML-Dokument signiert.
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

## Siehe auch

* Class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
