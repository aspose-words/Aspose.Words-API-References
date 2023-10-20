---
title: FileFormatInfo.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: 用于 .NET 的 Aspose.Words
description: FileFormatInfo LoadFormat 财产. 获取检测到的文档格式 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/fileformatinfo/loadformat/
---
## FileFormatInfo.LoadFormat property

获取检测到的文档格式

```csharp
public LoadFormat LoadFormat { get; }
```

## 评论

当 OOXML 文档被加密时，如果不首先解密它就无法确定它是 Excel、Word 还是 PowerPoint 文档，因此对于加密的 OOXML 文档，此属性将始终返回Docx.

## 例子

演示如何使用 FileFormatUtil 类来检测文档格式和加密。

```csharp
Document doc = new Document();

// 配置一个 SaveOptions 对象来加密文档
// 保存时输入密码，然后保存文档。
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// 验证我们文档的文件类型，以及它的加密状态。
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

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

演示如何使用 FileFormatUtil 方法来检测文档的格式。

```csharp
// 从缺少文件扩展名的文件中加载文档，然后检测其文件格式。
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // 下面是两种将 LoadFormat 转换为对应的 SaveFormat 的方法。
    // 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串中获取相应的 SaveFormat：
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - 将 LoadFormat 直接转换为其 SaveFormat：
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // 从流中加载一个文档，然后将其保存到自动检测到的文件扩展名。
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### 也可以看看

* enum [LoadFormat](../../loadformat/)
* class [FileFormatInfo](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
