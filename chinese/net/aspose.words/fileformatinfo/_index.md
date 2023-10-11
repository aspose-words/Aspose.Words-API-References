---
title: Class FileFormatInfo
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.FileFormatInfo 班级. 包含返回的数据FileFormatUtil文档格式检测方法.
type: docs
weight: 2810
url: /zh/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

包含返回的数据[`FileFormatUtil`](../fileformatutil/)文档格式检测方法.

要了解更多信息，请访问[检测文件格式并检查格式兼容性](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/)文档文章。

```csharp
public class FileFormatInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | 获取检测到的编码（如果适用于当前文档格式）。 目前仅检测 HTML 文档的编码。 |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | 返回`真的`如果该文档包含数字签名。 此属性仅通知文档上存在数字签名， 但不指定签名是否有效。 |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | 返回`真的`如果文档已加密并且需要密码才能打开。 |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | 获取检测到的文档格式。 |

### 评论

您不直接创建此类的实例。此类的对象由 返回[`DetectFileFormat`](../fileformatutil/detectfileformat/)方法。

### 例子

演示如何使用 FileFormatUtil 类来检测文档格式和加密。

```csharp
Document doc = new Document();

// 配置 SaveOptions 对象来加密文档
// 我们保存的时候带上密码，然后保存文档。
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// 验证文档的文件类型及其加密状态。
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

演示如何使用 FileFormatUtil 类来检测文档格式和数字签名的存在。

```csharp
// 使用 FileFormatInfo 实例验证文档是否未经过数字签名。
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// 使用新的 FileFormatInstance 来确认它已签名。
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// 我们可以像这样加载和访问集合中已签名文档的签名。
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


