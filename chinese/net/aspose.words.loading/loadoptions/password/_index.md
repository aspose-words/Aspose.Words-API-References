---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: 使用 LoadOptions 的 Password 属性轻松管理加密文档。安全地设置或检索您的密码，实现无缝访问。
type: docs
weight: 110
url: /zh/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

获取或设置打开加密文档的密码。 可以是`无效的`或空字符串。默认为`无效的`.

```csharp
public string Password { get; set; }
```

## 评论

您需要知道密码才能打开加密文档。如果文档未加密，请将其设置为`无效的`或空字符串。

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

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
