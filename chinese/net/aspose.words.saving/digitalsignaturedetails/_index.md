---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.DigitalSignatureDetails 类，实现无缝数字文档签名。轻松增强安全性和真实性！
type: docs
weight: 5640
url: /zh/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

包含使用数字签名签署文档的详细信息。

```csharp
public class DigitalSignatureDetails
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | 初始化一个新的实例`DigitalSignatureDetails`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | 获取或设置[`CertificateHolder`](./certificateholder/)包含用于签署文档的证书的对象。 |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | 获取或设置[`SignOptions`](./signoptions/)用于签署文档的对象。 |

## 例子

展示如何签署 OOXML 文档。

```csharp
Document doc = new Document(MyDir + "Document.docx");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
DigitalSignatureDetails digitalSignatureDetails = new DigitalSignatureDetails(
    certificateHolder,
    new SignOptions() { Comments = "Some comments", SignTime = DateTime.Now });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.DigitalSignatureDetails = digitalSignatureDetails;

Assert.AreEqual(certificateHolder, digitalSignatureDetails.CertificateHolder);
Assert.AreEqual("Some comments", digitalSignatureDetails.SignOptions.Comments);

doc.Save(ArtifactsDir + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
