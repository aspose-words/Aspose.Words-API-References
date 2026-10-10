---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel yöntemi"
linktitle: "get_XmlDsigLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel yöntemi. XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir. Varsayılan değer C++'ta XmlDSig'dir."
type: docs
weight: 8500
url: /tr/cpp/aspose.words.digitalsignatures/signoptions/get_xmldsiglevel/
---
## SignOptions::get_XmlDsigLevel method


XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir. Varsayılan değer [XmlDSig](../../xmldsiglevel/) dir.

```cpp
Aspose::Words::DigitalSignatures::XmlDsigLevel Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel() const
```


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

* Enum [XmlDsigLevel](../../xmldsiglevel/)
* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
