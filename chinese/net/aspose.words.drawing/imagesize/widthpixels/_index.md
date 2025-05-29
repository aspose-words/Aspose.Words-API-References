---
title: ImageSize.WidthPixels
linktitle: WidthPixels
articleTitle: WidthPixels
second_title: Aspose.Words for .NET
description: 发现 ImageSize WidthPixels 属性可以轻松检索图像的像素宽度，增强图像管理和优化。
type: docs
weight: 60
url: /zh/net/aspose.words.drawing/imagesize/widthpixels/
---
## ImageSize.WidthPixels property

获取图像的宽度（以像素为单位）。

```csharp
public int WidthPixels { get; }
```

## 例子

展示如何读取形状中图像的属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将包含从我们的本地文件系统获取的图像的形状插入到文档中。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// 如果形状包含图像，其 ImageData 属性将有效，
// 它将包含一个 ImageSize 对象。
ImageSize imageSize = shape.ImageData.ImageSize;

// ImageSize 对象包含有关形状内图像的只读信息。
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// 我们可以根据图像的大小来确定形状的大小，以避免拉伸图像。
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### 也可以看看

* class [ImageSize](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
