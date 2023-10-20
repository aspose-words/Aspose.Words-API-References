---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: 用于 .NET 的 Aspose.Words
description: MarkdownSaveOptions ExportImagesAsBase64 财产. 指定图像是否以 Base64 格式保存到输出文件 默认为错误的 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

指定图像是否以 Base64 格式保存到输出文件。 默认为`错误的`.

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## 评论

当此属性设置为`真的`图像数据直接导出到 **图像**不会创建元素和单独的文件。

## 例子

展示如何保存嵌入了图像的 .md 文档。

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
