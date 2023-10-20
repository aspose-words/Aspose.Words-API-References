---
title: PdfDigitalSignatureHashAlgorithm Enum
linktitle: PdfDigitalSignatureHashAlgorithm
articleTitle: PdfDigitalSignatureHashAlgorithm
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.PdfDigitalSignatureHashAlgorithm 枚举. 指定数字签名使用的数字哈希算法 在 C#.
type: docs
weight: 5440
url: /zh/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

指定数字签名使用的数字哈希算法。

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Sha256 | `0` | SHA-256 哈希算法。 |
| Sha384 | `1` | SHA-384 哈希算法。 |
| Sha512 | `2` | SHA-512 哈希算法。 |
| RipeMD160 | `3` | RIPEMD-160 哈希算法. |

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
