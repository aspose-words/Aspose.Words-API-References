---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words for .NET
description: 使用 ImageResolution 属性优化您的 Markdown 导出，设置自定义输出分辨率以获得更清晰的图像。默认值为 96 dpi。
type: docs
weight: 60
url: /zh/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

指定导出到 Markdown 时图像的输出分辨率。 默认值为`96 dpi`.

```csharp
public int ImageResolution { get; set; }
```

## 例子

显示如何设置图像的输出分辨率。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### 也可以看看

* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
