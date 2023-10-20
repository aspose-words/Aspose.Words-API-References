---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: 用于 .NET 的 Aspose.Words
description: RtfSaveOptions ExportCompactSize 财产. 允许使输出的 RTF 文档尺寸更小但如果它们包含 RTL从右到左文本它将无法正确显示 默认值为错误的 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

允许使输出的 RTF 文档尺寸更小，但如果它们包含 RTL（从右到左）文本，它将无法正确显示。 默认值为`错误的`.

```csharp
public bool ExportCompactSize { get; set; }
```

## 评论

如果要使用 Aspose.Words 转换为 RTF 的文档不包含阿拉伯语等语言的 从右到左的文本，则可以将此选项设置为`真的` 以减小生成的 RTF 的大小。

## 例子

展示如何使用自定义选项将文档保存为 .rtf。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 创建一个“RtfSaveOptions”对象以传递给文档的“Save”方法，以修改我们如何将其保存到 RTF。
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// 将“ExportCompactSize”属性设置为“true”以
// 以从右到左的文本兼容性为代价减小保存文档的大小。
options.ExportCompactSize = true;

// 将 "ExportImagesFotOldReaders" 属性设置为 "true" 以使用额外的关键字来确保我们的文档是
// 与 Microsoft Word 97 之前的阅读器和写字板兼容。
// 将“ExportImagesFotOldReaders”属性设置为“false”以减小文档的大小，
// 但要防止老读者能够阅读文档可能包含的任何非元文件或 BMP 图像。
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### 也可以看看

* class [RtfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
