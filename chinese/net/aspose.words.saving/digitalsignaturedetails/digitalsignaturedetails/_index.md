---
title: DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words for .NET
description: 发现 DigitalSignatureDetails 构造函数可以轻松初始化数字签名实例，从而增强应用程序的安全性和效率。
type: docs
weight: 10
url: /zh/net/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails constructor

初始化一个新的实例[`DigitalSignatureDetails`](../)类.

```csharp
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| certificateHolder | CertificateHolder | 包含证书本身的证书持有者。 |
| signOptions | SignOptions | 用于签署文件的签名选项。 |

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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
