---
title: ImageSize.HeightPixels
linktitle: HeightPixels
articleTitle: HeightPixels
second_title: Aspose.Words for .NET
description: 探索 ImageSize HeightPixels 属性，轻松访问和优化图像的像素高度，以获得更好的性能和质量。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/imagesize/heightpixels/
---
## ImageSize.HeightPixels property

获取图像的高度（以像素为单位）。

```csharp
public int HeightPixels { get; }
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
