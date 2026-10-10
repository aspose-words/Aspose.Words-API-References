---
title: "Aspose::Words::Loading::LoadOptions::get_Password 方法"
linktitle: "get_Password"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_Password 方法。获取或设置打开加密文档的密码。可以为 null 或空字符串。默认在 C++ 中为 null。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


获取或设置打开加密文档的密码。可以是 **null** 或空字符串。默认值为 **null**。

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## 备注


您需要知道密码才能打开加密文档。如果文档未加密，请将其设置为 **null** 或空字符串。

## 示例



展示如何对加密文档文件进行签名。
```cpp
// 从包含私钥的 PKCS#12 存储创建 X.509 证书。
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// 创建将在新数字签名中使用的注释、日期和解密密码。
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// 为未签名的输入文档设置本地系统文件名，并为其新的数字签名副本设置输出文件名。
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## 另见

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
