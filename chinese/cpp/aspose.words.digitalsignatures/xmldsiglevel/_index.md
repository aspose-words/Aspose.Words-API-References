---
title: "Aspose::Words::DigitalSignatures::XmlDsigLevel 枚举"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::XmlDsigLevel 枚举。指定基于 XML-DSig 标准的数字签名级别（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


根据 XML-DSig 标准指定数字签名的级别。

```cpp
enum class XmlDsigLevel
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| XmlDSig | 0 | 指定 XML-DSig 签名级别。 |
| XAdEsEpes | 1 | 指定 XAdES-EPES 签名级别。 |


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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
