---
title: FileFormatUtil.LoadFormatToSaveFormat
linktitle: LoadFormatToSaveFormat
articleTitle: LoadFormatToSaveFormat
second_title: 用于 .NET 的 Aspose.Words
description: FileFormatUtil LoadFormatToSaveFormat 方法. 转换LoadFormat值对一个SaveFormat如果可能的话值 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words/fileformatutil/loadformattosaveformat/
---
## FileFormatUtil.LoadFormatToSaveFormat method

转换[`LoadFormat`](../../loadformat/)值对一个[`SaveFormat`](../../saveformat/)如果可能的话值。

```csharp
public static SaveFormat LoadFormatToSaveFormat(LoadFormat loadFormat)
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 无法转换时抛出。 |

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

* enum [SaveFormat](../../saveformat/)
* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
