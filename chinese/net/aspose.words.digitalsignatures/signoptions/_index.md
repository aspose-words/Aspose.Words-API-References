---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.DigitalSignatures.SignOptions 类，使用灵活、安全的选项定制您的文档签名流程，从而增强工作流程。
type: docs
weight: 620
url: /zh/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

允许指定文档签名选项。

要了解更多信息，请访问[使用数字签名](https://docs.aspose.com/words/net/working-with-digital-signatures/)文档文章。

```csharp
public class SignOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [SignOptions](signoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | 指定数字签名的注释。 默认值为**空字符串**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | 解密源文档的密码。 默认值为**空字符串**(Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | 指定签名提供者的类 ID。 默认值为**空（全零）Guid**. |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | 签名行标识符。 默认值为**空（全零）Guid**. |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | 将在关联中显示的图像[`SignatureLine`](../../aspose.words.drawing/signatureline/). 默认值是`无效的`. |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | 签署日期。 默认值为**当前时间**(Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | 指定基于 XML-DSig 标准的数字签名级别。 默认值为XmlDSig. |

## 例子

展示如何对文档进行数字签名。

```csharp
// 从 PKCS#12 存储区创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建将与我们的新数字签名一起应用的评论和日期。
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// 通过文件流从本地文件系统获取未签名的文档，
// 然后根据输出文件流的文件名创建它的签名副本。
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### 也可以看看

* 命名空间 [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../)
