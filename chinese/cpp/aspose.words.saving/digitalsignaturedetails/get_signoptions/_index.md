---
title: "Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions 方法"
linktitle: "get_SignOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions 方法。获取或设置用于在 C++ 中对文档进行签名的 SignOptions 对象。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/digitalsignaturedetails/get_signoptions/
---
## DigitalSignatureDetails::get_SignOptions method


获取或设置用于签署文档的 [SignOptions](./) 对象。

```cpp
const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> & Aspose::Words::Saving::DigitalSignatureDetails::get_SignOptions() const
```


## 示例



展示如何对 OOXML 文档进行签名。
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

## 另见

* Class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* Class [DigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
