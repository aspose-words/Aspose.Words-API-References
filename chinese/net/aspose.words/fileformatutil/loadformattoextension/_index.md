---
title: FileFormatUtil.LoadFormatToExtension
linktitle: LoadFormatToExtension
articleTitle: LoadFormatToExtension
second_title: Aspose.Words for .NET
description: 使用 FileFormatUtil 的 LoadFormatToExtension 方法，轻松将加载格式值转换为文件扩展名。轻松获取准确的小写扩展名！
type: docs
weight: 60
url: /zh/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

将加载格式枚举值转换为文件扩展名。返回的扩展名是一个以点开头的小写字符串。

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 无法转换时抛出。 |

## 评论

这WordML值被转换为“.wml”。

## 例子

展示如何使用 FileFormatUtil 方法检测文档的格式。

```csharp
// 从缺少文件扩展名的文件中加载文档，然后检测其文件格式。
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // 以下是将 LoadFormat 转换为其对应的 SaveFormat 的两种方法。
    // 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串获取相应的 SaveFormat：
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - 将 LoadFormat 直接转换为其 SaveFormat：
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // 从流中加载文档，然后将其保存到自动检测的文件扩展名。
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### 也可以看看

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
