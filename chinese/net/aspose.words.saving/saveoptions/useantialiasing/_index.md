---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: 用于 .NET 的 Aspose.Words
description: SaveOptions UseAntiAliasing 财产. 获取或设置一个值确定是否使用抗锯齿进行渲染 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

获取或设置一个值，确定是否使用抗锯齿进行渲染。

```csharp
public bool UseAntiAliasing { get; set; }
```

## 评论

默认值为`错误的` .当此值设置为`真的`抗锯齿是 用于渲染。

当文档导出为以下格式时使用此属性： Tiff,Png,BmpJpeg,Emf .当文档导出到 Html,Mhtml和Epub 格式 此选项用于光栅图像。

## 例子

演示如何使用 SaveOptions 提高呈现文档的质量。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
