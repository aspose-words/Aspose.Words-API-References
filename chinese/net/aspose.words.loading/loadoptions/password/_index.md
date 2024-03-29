---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: 用于 .NET 的 Aspose.Words
description: LoadOptions Password 财产. 获取或设置打开加密文档的密码 可以无效的或空字符串默认为无效的 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

获取或设置打开加密文档的密码。 可以`无效的`或空字符串。默认为`无效的`.

```csharp
public string Password { get; set; }
```

## 评论

您需要知道密码才能打开加密文档。如果文档未加密，请将其设置为`无效的`或空字符串。

## 例子

演示如何签署加密的文档文件。

```csharp
// 从 PKCS#12 存储创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建评论、日期和解密密码，这些密码将与我们的新数字签名一起应用。
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// 为未签名的输入文档设置本地系统文件名，为其新的数字签名副本设置输出文件名。
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
