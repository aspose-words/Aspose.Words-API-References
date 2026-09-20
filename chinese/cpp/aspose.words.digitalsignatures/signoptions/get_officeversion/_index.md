---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion 方法"
linktitle: "get_OfficeVersion"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion 方法。获取或设置数字签名的 Office 版本。默认值在 C++ 中为 \"12.0\"。"
type: docs
weight: 4667
url: /zh/cpp/aspose.words.digitalsignatures/signoptions/get_officeversion/
---
## SignOptions::get_OfficeVersion method


获取或设置数字签名的 Office 版本。默认值为 "12.0"。

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion() const
```


## 示例



展示如何使用额外的签名选项对文档进行签名。
```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_WindowsVersion(u"10.0");
signOptions->set_ApplicationVersion(u"16.0.19127");
signOptions->set_OfficeVersion(u"16.0.19127/27");
signOptions->set_HorizontalResolution(1024);
signOptions->set_VerticalResolution(768);
signOptions->set_ColorDepth(24);

System::ArrayPtr<uint8_t> certBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"morzal.pfx");
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = Aspose::Words::DigitalSignatures::CertificateHolder::Create(certBytes, u"aw");
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DigitalSignatureUtil.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature> signature = signedDoc->get_DigitalSignatures()->idx_get(0);
ASSERT_EQ(1, signedDoc->get_DigitalSignatures()->get_Count());
ASSERT_TRUE(signature->get_IsValid());
ASSERT_EQ(u"10.0", signature->get_WindowsVersion());
ASSERT_EQ(u"16.0.19127", signature->get_ApplicationVersion());
ASSERT_EQ(u"16.0.19127/27", signature->get_OfficeVersion());
ASSERT_EQ(1024, signature->get_HorizontalResolution());
ASSERT_EQ(768, signature->get_VerticalResolution());
ASSERT_EQ(24, signature->get_ColorDepth());
```

## 另见

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
