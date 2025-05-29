---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words for .NET
description: 了解 MarkdownSaveOptions ExportImagesAsBase64 属性如何通过允许以 Base64 格式保存图像来增强输出文件。默认值为 false。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

指定是否将图像以 Base64 格式保存到输出文件。 默认值为`错误的`.

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## 评论

当此属性设置为`真的`图像数据直接导出到**图片**元素和单独的文件不会被创建。

## 例子

展示如何保存嵌入图像的 .md 文档。

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### 也可以看看

* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
