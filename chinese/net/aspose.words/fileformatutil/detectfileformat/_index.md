---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: 用于 .NET 的 Aspose.Words
description: FileFormatUtil DetectFileFormat 方法. 检测并返回有关存储在磁盘文件中的文档格式的信息 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

检测并返回有关存储在磁盘文件中的文档格式的信息。

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文件名。 |

### 返回值

A[`FileFormatInfo`](../../fileformatinfo/)包含检测到的信息的对象。

## 评论

即使此方法检测到文档格式，也不能保证 指定的文档有效。此方法仅通过 读取足以检测的数据来检测文档格式。要完全验证文档是否有效 ，您需要将文档加载到[`Document`](../../document/)目的。

这个方法抛出[`FileCorruptedException`](../../filecorruptedexception/)当格式被 识别时，但由于损坏而无法完成检测。

## 例子

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

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## DetectFileFormat(*Stream*) {#detectfileformat}

检测并返回有关存储在流中的文档格式的信息。

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 溪流。 |

### 返回值

A[`FileFormatInfo`](../../fileformatinfo/)包含检测到的信息的对象。

## 评论

该流必须位于文档的开头。

当该方法返回时，流中的位置将恢复到原始位置。

即使此方法检测到文档格式，也不能保证 指定的文档有效。此方法仅通过 读取足以检测的数据来检测文档格式。要完全验证文档是否有效 ，您需要将文档加载到[`Document`](../../document/)目的。

这个方法抛出[`FileCorruptedException`](../../filecorruptedexception/)当格式被 识别时，但由于损坏而无法完成检测。

## 例子

演示如何使用 FileFormatUtil 方法来检测文档的格式。

```csharp
// 从缺少文件扩展名的文件中加载文档，然后检测其文件格式。
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // 下面是将 LoadFormat 转换为其相应的 SaveFormat 的两种方法。
    // 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串获取相应的 SaveFormat：
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - 将 LoadFormat 直接转换为其 SaveFormat：
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // 从流中加载文档，然后将其保存到自动检测到的文件扩展名。
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### 也可以看看

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
