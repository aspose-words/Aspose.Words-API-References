---
title: "Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions metodo"
linktitle: "get_SignOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions metodo. Ottiene o imposta un oggetto SignOptions utilizzato per firmare un documento in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/digitalsignaturedetails/get_signoptions/
---
## DigitalSignatureDetails::get_SignOptions method


Ottiene o imposta un oggetto [SignOptions](./) utilizzato per firmare un documento.

```cpp
const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> & Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions() const
```


## Esempi



Mostra come firmare un documento OOXML.
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

## Vedi anche

* Class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
