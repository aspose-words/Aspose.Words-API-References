---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_Comments 方法"
linktitle: "get_Comments"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_Comments 方法。指定数字签名的注释。默认值在 C++ 中为空字符串。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.digitalsignatures/signoptions/get_comments/
---
## SignOptions::get_Comments method


指定数字签名的注释。默认值为 **empty string**。

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_Comments() const
```


## 示例



展示如何对文档进行数字签名。
```cpp
// 从包含私钥的 PKCS#12 存储创建 X.509 证书。
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// 创建将在新数字签名中使用的注释和日期。
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// 通过文件流从本地文件系统获取未签名的文档，
// 然后根据输出文件流的文件名创建其签名副本。
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## 另见

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
