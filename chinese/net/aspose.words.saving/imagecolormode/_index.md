---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.ImageColorMode 枚举，优化文档页面图像。控制色彩模式，提升项目的视觉质量。
type: docs
weight: 5960
url: /zh/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

指定生成的文档页面图像的颜色模式。

```csharp
public enum ImageColorMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 文档的页面将呈现为彩色图像。 |
| Grayscale | `1` | 文档的页面将呈现为灰度图像。 |
| BlackAndWhite | `2` | 文档页面将呈现为黑白图像。 |

## 例子

展示如何在渲染文档时设置颜色模式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
// 为保存操作将生成的图像选择一种颜色模式。
// 如果我们将“ImageColorMode”属性设置为“ImageColorMode.BlackAndWhite”，
// 保存操作将在渲染文档时应用灰度颜色减少。
 // 如果我们将“ImageColorMode”属性设置为“ImageColorMode.Grayscale”，
// 保存操作将把文档渲染为单色图像。
// 如果我们将“ImageColorMode”属性设置为“None”，则保存操作将应用默认方法
// 并在输出图像中保留所有文档的颜色。
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
