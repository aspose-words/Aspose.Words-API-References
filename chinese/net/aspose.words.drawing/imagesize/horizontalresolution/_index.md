---
title: ImageSize.HorizontalResolution
second_title: Aspose.Words for .NET API 参考
description: ImageSize 财产. 获取水平分辨率以 DPI 为单位
type: docs
weight: 40
url: /zh/net/aspose.words.drawing/imagesize/horizontalresolution/
---
## ImageSize.HorizontalResolution property

获取水平分辨率（以 DPI 为单位）。

```csharp
public double HorizontalResolution { get; }
```

### 例子

演示如何读取形状中图像的属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将一个形状插入到文档中，其中包含从本地文件系统获取的图像。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// 如果形状包含图像，则其 ImageData 属性将有效，
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
* 命名空间 [Aspose.Words.Drawing](../../imagesize/)
* 部件 [Aspose.Words](../../../)


