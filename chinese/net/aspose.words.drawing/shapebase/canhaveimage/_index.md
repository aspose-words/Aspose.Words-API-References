---
title: ShapeBase.CanHaveImage
second_title: Aspose.Words for .NET API 参考
description: ShapeBase 财产. 如果形状类型允许形状具有图像则返回 true
type: docs
weight: 100
url: /zh/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

如果形状类型允许形状具有图像，则返回 true。

```csharp
public bool CanHaveImage { get; }
```

### 评论

尽管 Microsoft Word 有一种特殊的图像形状类型，但似乎在 Microsoft Word 文档中，除了组形状之外的任何 shape 都可以有图像，因此该属性对所有形状返回 true，除了[`GroupShape`](../../groupshape/).

### 例子

显示如何插入和旋转图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入带有图像的形状。
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// 将图像顺时针旋转 45 度。
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../shapebase/)
* 部件 [Aspose.Words](../../../)


