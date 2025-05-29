---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: 探索 ImageSaveOptions Clone 方法，轻松创建对象的深度克隆，提高编码效率和灵活性。
type: docs
weight: 210
url: /zh/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

创建此对象的深度克隆。

```csharp
public ImageSaveOptions Clone()
```

## 例子

展示如何选择将文档渲染为图像的每像素位数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
// 为保存操作将生成的图像选择像素格式。
// 不同的每像素比特率将影响生成图像的质量和文件大小。
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// 我们可以克隆 ImageSaveOptions 实例。
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### 也可以看看

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
