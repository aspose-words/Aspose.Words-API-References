---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.PdfDigitalSignatureDetails 班级. 包含使用数字签名签署 PDF 文档的详细信息 在 C#.
type: docs
weight: 5430
url: /zh/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

包含使用数字签名签署 PDF 文档的详细信息。

```csharp
public class PdfDigitalSignatureDetails
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | 初始化此类的实例。 |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) | 初始化此类的实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | 返回包含用于签署文档的证书的证书持有者对象。 |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | 获取或设置哈希算法。 |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | 获取或设置签名的位置。 |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | 获取或设置签名的原因。 |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | 获取或设置签名日期。 |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | 获取或设置数字签名时间戳设置。 |

## 评论

目前，数字签名 PDF 文档仅适用于 .NET 2.0 或更高版本。

要在 Aspose.Words 创建 PDF 文档时对其进行数字签名，请设置[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) 属性为有效`PdfDigitalSignatureDetails`对象，然后将文档保存为 PDF 格式，传递 [`PdfSaveOptions`](../pdfsaveoptions/)作为参数传入[`Save`](../../aspose.words/document/save/)方法。

Aspose.Words 在整个 PDF 文档上创建 PKCS#7 签名，并在创建数字签名时使用“Adobe.PPKMS”过滤器和 “adbe.pkcs7.sha1”子过滤器。

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
