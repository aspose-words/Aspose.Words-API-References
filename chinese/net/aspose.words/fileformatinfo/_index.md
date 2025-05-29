---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.FileFormatInfo 类，高效检测文档格式。访问详细数据，增强您的文件管理解决方案。
type: docs
weight: 3220
url: /zh/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

包含由[`FileFormatUtil`](../fileformatutil/)文档格式检测方法.

要了解更多信息，请访问[检测文件格式并检查格式兼容性](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/)文档文章。

```csharp
public class FileFormatInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | 如果适用于当前文档格式，则获取检测到的编码。 目前仅检测 HTML 文档的编码。 |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | 返回`真的`如果此文档包含数字签名。 此属性仅告知文档上存在数字签名， 但它并未指定签名是否有效。 |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | 返回`真的`如果此文档包含 VBA 宏。 |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | 返回`真的`如果文档已加密并需要密码才能打开。 |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | 获取检测到的文档格式。 |

## 评论

您不能直接创建此类的实例。此类的对象由 返回[`DetectFileFormat`](../fileformatutil/detectfileformat/)方法。

## 例子

展示如何使用 FileFormatUtil 类检测文档格式和加密。

```csharp
Document doc = new Document();

// 配置一个 SaveOptions 对象来加密文档
// 保存时使用密码，然后保存文档。
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// 验证我们文档的文件类型及其加密状态。
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

展示如何使用 FileFormatUtil 类检测文档格式和数字签名的存在。

```csharp
// 使用 FileFormatInfo 实例来验证文档是否未经数字签名。
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// 使用新的 FileFormatInstance 来确认它已签名。
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// 我们可以像这样在集合中加载和访问已签名文档的签名。
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
