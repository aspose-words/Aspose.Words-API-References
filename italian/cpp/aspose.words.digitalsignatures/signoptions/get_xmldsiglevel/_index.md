---
title: "metodo Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel"
linktitle: "get_XmlDsigLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel. Specifica il livello di una firma digitale basato sullo standard XML-DSig. Il valore predefinito è XmlDSig in C++."
type: docs
weight: 8500
url: /it/cpp/aspose.words.digitalsignatures/signoptions/get_xmldsiglevel/
---
## SignOptions::get_XmlDsigLevel method


Specifica il livello di una firma digitale basato sullo standard XML-DSig. Il valore predefinito è [XmlDSig](../../xmldsiglevel/).

```cpp
Aspose::Words::DigitalSignatures::XmlDsigLevel Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel() const
```


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

* Enum [XmlDsigLevel](../../xmldsiglevel/)
* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
