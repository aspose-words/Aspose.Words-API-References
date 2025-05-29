---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words for .NET
description: 探索 SaveOptions 的 UseAntiAliasing 属性，提升渲染质量。控制抗锯齿效果，获得更流畅的视觉效果和更佳的性能。
type: docs
weight: 200
url: /zh/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

获取或设置一个值，确定是否使用抗锯齿进行渲染。

```csharp
public bool UseAntiAliasing { get; set; }
```

## 评论

默认值为`错误的` 。当此值设置为`真的`抗锯齿 is 用于渲染。

当文档导出为以下格式时使用此属性： Tiff，Png，Bmp , Jpeg，Emf . 当文档导出到 Html，Mhtml , Epub，Azw3 或Mobi格式此选项用于光栅图像。

## 例子

展示如何使用 SaveOptions 提高渲染文档的质量。

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
