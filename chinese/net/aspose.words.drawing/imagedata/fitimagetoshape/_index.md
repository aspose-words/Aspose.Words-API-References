---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words for .NET
description: 使用 FitImageToShape 方法优化您的图像，确保 Shape 框架内的完美纵横比对齐，以获得令人惊叹的视觉呈现。
type: docs
weight: 190
url: /zh/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

将图像数据适合 Shape 框架，以便图像数据的纵横比与 Shape 框架的纵横比相匹配。

```csharp
public void FitImageToShape()
```

## 例子

显示如何将图像数据适合形状框架。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入图像形状并保持其方向为默认状态。
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
