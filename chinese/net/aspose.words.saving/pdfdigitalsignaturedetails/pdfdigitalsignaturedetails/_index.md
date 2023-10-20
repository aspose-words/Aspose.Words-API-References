---
title: PdfDigitalSignatureDetails
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: 用于 .NET 的 Aspose.Words
description: PdfDigitalSignatureDetails 构造函数. 初始化此类的实例 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/pdfdigitalsignaturedetails/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails() {#constructor}

初始化此类的实例。

```csharp
public PdfDigitalSignatureDetails()
```

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

---

## PdfDigitalSignatureDetails(*[CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) {#constructor_1}

初始化此类的实例。

```csharp
public PdfDigitalSignatureDetails(CertificateHolder certificateHolder, string reason, 
    string location, DateTime signatureDate)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| certificateHolder | CertificateHolder | 包含证书本身的证书持有者。 |
| reason | String | 签名的原因。 |
| location | String | 签字地点。 |
| signatureDate | DateTime | 签署的日期和时间。 |

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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [PdfDigitalSignatureDetails](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
