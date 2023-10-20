---
title: PdfDigitalSignatureDetails.Reason
linktitle: Reason
articleTitle: Reason
second_title: 用于 .NET 的 Aspose.Words
description: PdfDigitalSignatureDetails Reason 财产. 获取或设置签名的原因 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.saving/pdfdigitalsignaturedetails/reason/
---
## PdfDigitalSignatureDetails.Reason property

获取或设置签名的原因。

```csharp
public string Reason { get; set; }
```

## 评论

默认值为`无效的`.

## 例子

演示如何签署生成的 PDF 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“SaveOptions”对象的“DigitalSignatureDetails”对象配置为
// 当我们使用“Save”方法呈现文档时对文档进行数字签名。
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### 也可以看看

* class [PdfDigitalSignatureDetails](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
