---
title: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum"
linktitle: "XmlDsigLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum. Specifica il livello di una firma digitale basato sullo standard XML-DSig in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


Specifica il livello di una firma digitale basato sullo standard XML-DSig.

```cpp
enum class XmlDsigLevel
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| XmlDSig | 0 | Specifica il livello della firma XML-DSig. |
| XAdEsEpes | 1 | Specifica il livello della firma XAdES-EPES. |


## Esempi



Mostra come firmare un documento basato sullo standard XML-DSig.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Vedi anche

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
