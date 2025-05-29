---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words for .NET
description: 探索 ShapeBase 旋转属性，轻松定义和自定义形状的旋转角度，增强设计的精确度和创造力。
type: docs
weight: 500
url: /zh/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

定义形状旋转的角度（以度为单位）。 正值对应顺时针旋转角度。

```csharp
public double Rotation { get; set; }
```

## 评论

默认值为 0。

## 例子

展示如何插入和旋转图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入带有图像的形状。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// 将图像顺时针旋转 45 度。
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
