---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel 方法"
linktitle: "get_XmlDsigLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel 方法。指定基于 XML-DSig 标准的数字签名级别。默认值为 XmlDSig，在 C++ 中。"
type: docs
weight: 8500
url: /zh/cpp/aspose.words.digitalsignatures/signoptions/get_xmldsiglevel/
---
## SignOptions::get_XmlDsigLevel method


指定基于 XML-DSig 标准的数字签名级别。默认值为 [XmlDSig](../../xmldsiglevel/)。

```cpp
Aspose::Words::DigitalSignatures::XmlDsigLevel Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel() const
```


## 示例



展示如何基于 XML-DSig 标准对文档进行签名。
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## 另见

* Enum [XmlDsigLevel](../../xmldsiglevel/)
* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
