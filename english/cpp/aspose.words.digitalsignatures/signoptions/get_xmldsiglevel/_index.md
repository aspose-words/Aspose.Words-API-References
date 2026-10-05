---
title: Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel method
linktitle: get_XmlDsigLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel method. Specifies the level of a digital signature based on the XML-DSig standard. The default value is XmlDSig in C++.'
type: docs
weight: 8500
url: /cpp/aspose.words.digitalsignatures/signoptions/get_xmldsiglevel/
---
## SignOptions::get_XmlDsigLevel method


Specifies the level of a digital signature based on the XML-DSig standard. The default value is [XmlDSig](../../xmldsiglevel/).

```cpp
Aspose::Words::DigitalSignatures::XmlDsigLevel Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel() const
```

## Remarks


Different levels of XAdES signatures can be created starting with Office 2010.

This is only relevant for the following document formats: DOC, DOCX, and XPS. It is ignored in other document formats, which always produce a plain XML-DSig signature regardless of this setting.

## Examples



Shows how to sign document based on XML-DSig standard. 
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## See Also

* Enum [XmlDsigLevel](../../xmldsiglevel/)
* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
