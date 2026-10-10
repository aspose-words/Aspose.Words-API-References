---
title: "Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails method"
linktitle: "get_DigitalSignatureDetails"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails method. 获取或设置用于在 C++ 中对文档签名的 DigitalSignatureDetails 对象。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words.saving/xpssaveoptions/get_digitalsignaturedetails/
---
## XpsSaveOptions::get_DigitalSignatureDetails method


获取或设置用于对文档签名的 [DigitalSignatureDetails](../../digitalsignaturedetails/) 对象。

```cpp
const System::SharedPtr<Aspose::Words::Saving::DigitalSignatureDetails> & Aspose::Words::Saving::XpsSaveOptions::get_DigitalSignatureDetails() const
```


## 示例



展示如何对 XPS 文档进行签名。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto options = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
options->set_SignTime(System::DateTime::get_Now());
options->set_Comments(u"Some comments");

auto digitalSignatureDetails = System::MakeObject<Aspose::Words::Saving::DigitalSignatureDetails>(certificateHolder, options);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
saveOptions->set_DigitalSignatureDetails(digitalSignatureDetails);

ASPOSE_ASSERT_EQ(certificateHolder, digitalSignatureDetails->get_CertificateHolder());
ASSERT_EQ(u"Some comments", digitalSignatureDetails->get_SignOptions()->get_Comments());

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.XpsDigitalSignature.docx", saveOptions);
```

## 另见

* Class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
