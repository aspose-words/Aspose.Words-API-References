---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_DigitalSignatureDetails metodo"
linktitle: "get_DigitalSignatureDetails"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_DigitalSignatureDetails metodo. Ottiene o imposta l'oggetto DigitalSignatureDetails utilizzato per firmare un documento in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words.saving/ooxmlsaveoptions/get_digitalsignaturedetails/
---
## OoxmlSaveOptions::get_DigitalSignatureDetails method


Ottiene o imposta l'oggetto [DigitalSignatureDetails](../../digitalsignaturedetails/) usato per firmare un documento.

```cpp
const System::SharedPtr<Aspose::Words::Saving::DigitalSignatureDetails> & Aspose::Words::Saving::OoxmlSaveOptions::get_DigitalSignatureDetails() const
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

* Class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
