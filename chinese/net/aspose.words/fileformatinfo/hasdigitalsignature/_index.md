---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words for .NET
description: 发现 FileFormatInfo HasDigitalSignature 属性——快速检查您的文档是否包含数字签名，增强安全性和真实性。
type: docs
weight: 20
url: /zh/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

返回`真的`如果此文档包含数字签名。 此属性仅告知文档上存在数字签名， 但它并未指定签名是否有效。

```csharp
public bool HasDigitalSignature { get; }
```

## 评论

此属性可帮助您区分已进行数字签名的文档和未进行数字签名的文档。 如果您使用 Aspose.Words 修改并保存已进行数字签名的文档，则数字签名将会丢失。 这是设计使然，因为数字签名的存在是为了保护文档的真实性。 使用此属性，您可以在处理已进行数字签名的文档之前像处理普通文档一样检测这些文档，并采取一些措施来避免丢失数字签名，例如通知用户。

## 例子

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

* class [FileFormatInfo](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
