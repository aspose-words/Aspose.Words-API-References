---
title: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum. Anger nivån för en digital signatur baserad på XML-DSig-standarden i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


Anger nivån för en digital signatur baserat på XML-DSig-standarden.

```cpp
enum class XmlDsigLevel
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| XmlDSig | 0 | Anger XML-DSig-signaturnivå. |
| XAdEsEpes | 1 | Anger XAdES-EPES-signaturnivå. |


## Exempel



Visar hur man signerar ett dokument baserat på XML-DSig-standarden.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Se även

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
