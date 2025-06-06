---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: Aspose.Words for .NET
description: 使用 UseHighQualityRendering 属性优化您的 SaveOptions，以获得更佳的输出效果。控制渲染速度和质量，获得完美效果。
type: docs
weight: 210
url: /zh/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

获取或设置一个值，确定是否使用高质量（即慢速）渲染算法。

```csharp
public bool UseHighQualityRendering { get; set; }
```

## 评论

默认值为`错误的`.

当文档导出为图像格式时使用此属性： Tiff，Png，Bmp , Jpeg，Emf。

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
