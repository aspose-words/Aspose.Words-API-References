---
title: "Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails costruttore"
linktitle: "DigitalSignatureDetails"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails costruttore. Inizializza una nuova istanza della classe DigitalSignatureDetails in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails::DigitalSignatureDetails constructor


Inizializza una nuova istanza della classe [DigitalSignatureDetails](../).

```cpp
Aspose::Words::Saving::DigitalSignatureDetails::DigitalSignatureDetails(const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certificateHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certificateHolder | const System::SharedPtr\\<Aspose::Words::DigitalSignatures::CertificateHolder\\>\\& | Un contenitore di certificati che contiene il certificato stesso. |
| signOptions | const System::SharedPtr\\<Aspose::Words::DigitalSignatures::SignOptions\\>\\& | Opzioni di firma da utilizzare per firmare un documento. |

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

* Class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* Class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
