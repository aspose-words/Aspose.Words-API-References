---
title: OoxmlSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words for .NET
description: 探索 OoxmlSaveOptions 的 DigitalSignatureDetails 属性，以有效管理数字签名，实现安全文档签名和增强合规性。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/digitalsignaturedetails/
---
## OoxmlSaveOptions.DigitalSignatureDetails property

获取或设置[`DigitalSignatureDetails`](../../digitalsignaturedetails/)用于签署文档的对象。

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
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

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [OoxmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
