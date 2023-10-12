---
title: ShapeBase.DistanceTop
second_title: Aspose.Words for .NET API 参考
description: ShapeBase 财产. 返回或设置文档文本与形状上边缘之间的距离以磅为单位
type: docs
weight: 160
url: /zh/net/aspose.words.drawing/shapebase/distancetop/
---
## ShapeBase.DistanceTop property

返回或设置文档文本与形状上边缘之间的距离（以磅为单位）。

```csharp
public double DistanceTop { get; set; }
```

### 评论

默认值为 0。

仅对顶级形状有效。

### 例子

演示如何设置围绕形状的文本的环绕距离。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个矩形，并使文本紧紧围绕其边界。
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// 将形状和周围文本之间的最小距离设置为四边 40pt。
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// 将形状移近页面中心，然后顺时针旋转形状 60 度。
shape.Top = 75;
shape.Left = 150; 
shape.Rotation = 60;

// 添加环绕形状的文本。
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../shapebase/)
* 部件 [Aspose.Words](../../../)


