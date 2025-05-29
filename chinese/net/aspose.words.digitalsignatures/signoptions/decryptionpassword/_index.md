---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words for .NET
description: 使用 SignOptions 的 DecryptionPassword 功能轻松解锁您的文档。轻松安全地解密源文件；默认值为空字符串。
type: docs
weight: 30
url: /zh/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

解密源文档的密码。 默认值为**空字符串**(Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## 评论

如果 OOXML 文档已加密，则应提供解密密码 以解密源文档，然后才能对其进行签名。 对于二进制 DOC 格式的文档，则不需要执行此操作。

## 例子

显示如何签署加密文档文件。

```csharp
// 从 PKCS#12 存储区创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建将与我们的新数字签名一起应用的评论、日期和解密密码。
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// 为未签名的输入文档设置本地系统文件名，并为其新的数字签名副本设置输出文件名。
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### 也可以看看

* class [SignOptions](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
