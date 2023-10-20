---
title: FileFormatUtil.SaveFormatToExtension
linktitle: SaveFormatToExtension
articleTitle: SaveFormatToExtension
second_title: 用于 .NET 的 Aspose.Words
description: FileFormatUtil SaveFormatToExtension 方法. 将保存格式枚举值转换为文件扩展名返回的扩展名是带有前导点的小写字符串 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil.SaveFormatToExtension method

将保存格式枚举值转换为文件扩展名。返回的扩展名是带有前导点的小写字符串。

```csharp
public static string SaveFormatToExtension(SaveFormat saveFormat)
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 无法转换时抛出。 |

## 评论

这WordML值转换为“.wml”。

这FlatOpc值转换为“.fopc”。

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
* class [FileFormatUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
