---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: 用于 .NET 的 Aspose.Words
description: FileFormatInfo HasDigitalSignature 财产. 返回真的如果该文档包含数字签名 此属性仅通知文档上存在数字签名 但不指定签名是否有效 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

返回`真的`如果该文档包含数字签名。 此属性仅通知文档上存在数字签名， 但不指定签名是否有效。

```csharp
public bool HasDigitalSignature { get; }
```

## 评论

此属性的存在是为了帮助您对经过数字签名的文档和未经数字签名的文档进行排序。 如果您使用 Aspose.Words 修改并保存经过数字签名的文档，则数字签名将 丢失。这是设计使然，因为数字签名的存在是为了保护文档的真实性。 使用此属性，您可以在以与普通 文档相同的方式处理数字签名文档之前检测它们，并采取一些操作以避免丢失数字签名，例如通知用户。

## 例子

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

* class [FileFormatInfo](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
