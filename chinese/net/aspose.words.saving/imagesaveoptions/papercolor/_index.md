---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: 用于 .NET 的 Aspose.Words
description: ImageSaveOptions PaperColor 财产. 获取或设置生成图像的背景纸张颜色 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

获取或设置生成图像的背景（纸张）颜色。

默认值为White。

```csharp
public Color PaperColor { get; set; }
```

## 评论

当渲染指定其自身背景颜色的文档页面时， 则文档背景颜色将覆盖此属性指定的颜色。

## 例子

将Word文档的页面渲染为具有透明或彩色背景的图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// 将“PaperColor”属性设置为透明颜色以应用透明
// 将文档渲染为图像时的背景。
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// 将“PaperColor”属性设置为不透明颜色以应用该颜色
// 作为我们将文档渲染为图像时的背景。
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### 也可以看看

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
