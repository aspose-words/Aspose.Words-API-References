---
title: DigitalSignatureDetails.SignOptions
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words for .NET
description: 了解 DigitalSignatureDetails SignOptions 属性如何通过轻松管理无缝数字签名的签名选项来增强文档安全性。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/digitalsignaturedetails/signoptions/
---
## DigitalSignatureDetails.SignOptions property

获取或设置`SignOptions`用于签署文档的对象。

```csharp
public SignOptions SignOptions { get; set; }
```

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

* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
