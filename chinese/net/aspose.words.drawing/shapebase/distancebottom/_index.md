---
title: ShapeBase.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words for .NET
description: 发现 ShapeBase DistanceBottom 属性，轻松设置和调整文档文本和形状底边之间的点间隙，以实现最佳布局。
type: docs
weight: 130
url: /zh/net/aspose.words.drawing/shapebase/distancebottom/
---
## ShapeBase.DistanceBottom property

返回或设置文档文本和形状底边之间的距离（以点为单位）。

```csharp
public double DistanceBottom { get; set; }
```

## 评论

默认值为 0。

仅对顶层形状有效。

## 例子

展示如何设置形状周围文本的环绕距离。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个矩形，并让文本紧紧环绕其边界。
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// 将形状和周围文本之间的最小距离设置为所有边的 40pt。
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
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
