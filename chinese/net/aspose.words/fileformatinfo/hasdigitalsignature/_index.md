---
title: FileFormatInfo.HasDigitalSignature
second_title: Aspose.Words for .NET API 参考
description: FileFormatInfo 财产. 如果此文档包含数字签名则返回 true 此属性仅告知文档上存在数字签名 但并未指定签名是否有效
type: docs
weight: 20
url: /zh/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

如果此文档包含数字签名，则返回 true。 此属性仅告知文档上存在数字签名， ，但并未指定签名是否有效。

```csharp
public bool HasDigitalSignature { get; }
```

### 评论

此属性的存在是为了帮助您将经过数字签名的文档与未经过数字签名的文档进行排序。 如果您使用 Aspose.Words 修改并保存经过数字签名的文档，则数字签名将 丢失。这是设计使然，因为存在数字签名以保护文档的真实性。 使用此属性，您可以在以与正常 文档相同的方式处理它们之前检测数字签名的文档，并采取一些措施来避免丢失数字签名，例如通知用户。

### 例子

演示如何使用 FileFormatUtil 类来检测文档格式和数字签名的存在。

```csharp
// 使用 FileFormatInfo 实例来验证文档是否没有经过数字签名。
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// 使用一个新的 FileFormatInstance 来确认它是签名的。
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// 我们可以在这样的集合中加载和访问已签名文档的签名。
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### 也可以看看

* class [FileFormatInfo](../)
* 命名空间 [Aspose.Words](../../fileformatinfo/)
* 部件 [Aspose.Words](../../../)


