---
title: PdfDigitalSignatureTimestampSettings.ServerUrl
linktitle: ServerUrl
articleTitle: ServerUrl
second_title: 用于 .NET 的 Aspose.Words
description: PdfDigitalSignatureTimestampSettings ServerUrl 财产. 时间戳服务器 URL 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/
---
## PdfDigitalSignatureTimestampSettings.ServerUrl property

时间戳服务器 URL.

```csharp
public string ServerUrl { get; set; }
```

## 评论

默认值为`无效的` . 如果`无效的`，那么数字签名将不会被加上时间戳。

## 例子

演示如何对保存的 PDF 文档进行数字签名并为其添加时间戳。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 创建数字签名并将其分配给我们的 SaveOptions 对象，以便在将文档保存为 PDF 时对文档进行签名。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// 创建经过权威验证的时间戳时间戳。
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// 时间戳的默认生命周期是100秒。
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// 我们可以通过构造函数设置超时时间。
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// 此时“Save”方法会将我们的签名应用到输出文档中。
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### 也可以看看

* class [PdfDigitalSignatureTimestampSettings](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
