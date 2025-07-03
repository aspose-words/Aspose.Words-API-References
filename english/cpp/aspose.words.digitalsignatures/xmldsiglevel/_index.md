---
title: Aspose::Words::DigitalSignatures::XmlDsigLevel enum
linktitle: XmlDsigLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::XmlDsigLevel enum. Specifies the level of a digital signature based on XML-DSig standard in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


Specifies the level of a digital signature based on XML-DSig standard.

```cpp
enum class XmlDsigLevel
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| XmlDSig | 0 | Specifies XML-DSig signature level. |
| XAdEsEpes | 1 | Specifies XAdES-EPES signature level. |


## Examples



Shows how to sign document based on XML-DSig standard. 
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## See Also

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
