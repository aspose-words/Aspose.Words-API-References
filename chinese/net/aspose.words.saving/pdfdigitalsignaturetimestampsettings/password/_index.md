---
title: PdfDigitalSignatureTimestampSettings.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: 使用 PdfDigitalSignatureTimestampSettings 保护您的 PDF 文档。轻松管理时间戳服务器密码，增强保护和合规性。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/
---
## PdfDigitalSignatureTimestampSettings.Password property

时间戳服务器密码。

```csharp
public string Password { get; set; }
```

## 评论

默认值为`无效的`.

## 例子

展示如何对已保存的 PDF 文档进行数字签名并添加时间戳。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 创建一个数字签名并将其分配给我们的 SaveOptions 对象，以便在我们将文档保存为 PDF 时对其进行签名。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// 创建经过时间戳权威验证的时间戳。
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// 时间戳的默认寿命为100秒。
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// 我们可以通过构造函数设置超时时间。
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr”，选项.DigitalSignatureDetails.TimestampSettings.ServerUrl）；
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// 此时，“Save”方法将把我们的签名应用到输出文档。
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### 也可以看看

* class [PdfDigitalSignatureTimestampSettings](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
