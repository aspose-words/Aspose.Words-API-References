---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: 用于 .NET 的 Aspose.Words
description: RtfSaveOptions ExportImagesForOldReaders 财产. 指定老读者的关键字是否写入 RTF 这会显着影响 RTF 文档的大小 默认值为真的 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

指定“老读者”的关键字是否写入 RTF。 这会显着影响 RTF 文档的大小。 默认值为`真的`.

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## 评论

“老读者”是 Microsoft Word 97 之前的应用程序以及写字板。 当此选项打开时`真的`Aspose.Words 写入额外的 RTF 关键字。 这些关键字允许文档在 “旧阅读器”应用程序中打开时正确显示，但会显着增加文档的大小。

如果您将此选项设置为`错误的`，那么“旧阅读器”中将只显示 WMF、EMF 和 BMP 格式 的图像。

## 例子

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
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
