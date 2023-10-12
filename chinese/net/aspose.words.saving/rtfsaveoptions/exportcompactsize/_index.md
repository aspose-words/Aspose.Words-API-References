---
title: RtfSaveOptions.ExportCompactSize
second_title: Aspose.Words for .NET API 参考
description: RtfSaveOptions 财产. 允许缩小输出 RTF 文档的大小但如果它们包含 RTL从右到左文本则将无法正确显示 默认值为错误的.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

允许缩小输出 RTF 文档的大小，但如果它们包含 RTL（从右到左）文本，则将无法正确显示。 默认值为`错误的`.

```csharp
public bool ExportCompactSize { get; set; }
```

### 评论

如果您要使用 Aspose.Words 转换为 RTF 的文档不包含阿拉伯语等语言中的 从右到左文本，那么您可以将此选项设置为`真的` 以减小生成的 RTF 的大小。

### 例子

演示如何使用自定义选项将文档保存为 .rtf。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 创建一个“RtfSaveOptions”对象传递给文档的“Save”方法来修改我们将其保存为 RTF 的方式。
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// 将“ExportCompactSize”属性设置为“true”即可
// 以从右到左的文本兼容性为代价来减小保存文档的大小。
options.ExportCompactSize = true;

// 将“ExportImagesFotOldReaders”属性设置为“true”以使用额外的关键字来确保我们的文档
// 与 Microsoft Word 97 之前的阅读器和写字板兼容。
// 将“ExportImagesFotOldReaders”属性设置为“false”以减小文档的大小，
// 但防止老读者能够读取文档可能包含的任何非图元文件或 BMP 图像。
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### 也可以看看

* class [RtfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../rtfsaveoptions/)
* 部件 [Aspose.Words](../../../)


