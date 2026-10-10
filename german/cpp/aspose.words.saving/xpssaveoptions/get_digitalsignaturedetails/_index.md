---
title: "Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails Methode"
linktitle: "get_DigitalSignatureDetails"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails Methode. Ruft das DigitalSignatureDetails-Objekt ab oder legt es fest, das zum Signieren eines Dokuments in C++ verwendet wird."
type: docs
weight: 2500
url: /de/cpp/aspose.words.saving/xpssaveoptions/get_digitalsignaturedetails/
---
## XpsSaveOptions::get_DigitalSignatureDetails method


Ruft das [DigitalSignatureDetails](../../digitalsignaturedetails/) Objekt ab oder legt es fest, das zum Signieren eines Dokuments verwendet wird.

```cpp
const System::SharedPtr<Aspose::Words::Saving::DigitalSignatureDetails> & Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails() const
```


## Beispiele



Zeigt, wie man ein XPS-Dokument signiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto options = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
options->set_SignTime(System::DateTime::get_Now());
options->set_Comments(u"Some comments");

auto digitalSignatureDetails = System::MakeObject<Aspose::Words::Saving::DigitalSignatureDetails>(certificateHolder, options);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
saveOptions->set_DigitalSignatureDetails(digitalSignatureDetails);

ASPOSE_ASSERT_EQ(certificateHolder, digitalSignatureDetails->get_CertificateHolder());
ASSERT_EQ(u"Some comments", digitalSignatureDetails->get_SignOptions()->get_Comments());

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.XpsDigitalSignature.docx", saveOptions);
```

## Siehe auch

* Class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
