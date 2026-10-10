---
title: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum"
linktitle: "XmlDsigLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum. C++'da XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir.

```cpp
enum class XmlDsigLevel
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| XmlDSig | 0 | XML-DSig imza seviyesini belirtir. |
| XAdEsEpes | 1 | XAdES-EPES imza seviyesini belirtir. |


## Örnekler



XML-DSig standardına dayalı belgeyi nasıl imzalayacağınızı gösterir.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
