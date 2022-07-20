---
title: Bottom
second_title: Aspose.Words for .NET API 参考
description: 获取形状包含块的底边位置
type: docs
weight: 60
url: /zh/net/aspose.words.drawing/shapebase/bottom/
---
## ShapeBase.Bottom property

获取形状包含块的底边位置。

```csharp
public double Bottom { get; }
```

### 评论

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

### 例子

显示如何插入浮动图像，并指定其位置和大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// 配置形状的“RelativeHorizontalPosition”属性来处理“Left”属性的值
// 作为形状从页面左侧的水平距离，以磅为单位。
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// 设置形状到页面左侧的水平距离为 100。
shape.Left = 100;

// 以类似的方式使用“RelativeVerticalPosition”属性将形状定位在页面顶部下方 80pt 处。
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// 设置形状的高度，它将自动缩放宽度以保留尺寸。
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// "Bottom" 和 "Right" 属性包含图像的底部和右侧边缘。
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### 也可以看看

* class [ShapeBase](../../shapebase)
* 命名空间 [Aspose.Words.Drawing](../../shapebase)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->