---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words for .NET
description: 探索 ShapeBase CanHaveImage 属性——了解如何确定您的形状类型是否支持图像以增强视觉吸引力！
type: docs
weight: 100
url: /zh/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

返回`真的`如果形状类型允许形状具有图像。

```csharp
public bool CanHaveImage { get; }
```

## 评论

尽管 Microsoft Word 具有用于图像的特殊形状类型，但在 Microsoft Word 文档中，除组形状之外的任何 shape 都可以有图像，因此此属性返回`真的`除以下所有形状外[`GroupShape`](../../groupshape/)。

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
