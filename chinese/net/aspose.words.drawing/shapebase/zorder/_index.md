---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase ZOrder 财产. 确定重叠形状的显示顺序 在 C#.
type: docs
weight: 610
url: /zh/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

确定重叠形状的显示顺序。

```csharp
public int ZOrder { get; set; }
```

## 评论

仅对顶级形状有效。

默认值为 0。

数字代表堆叠优先级。数字较大的形状将显示 ，就好像它与数字较小的形状重叠（在“前面”）。

重叠形状的顺序与文档标题和 main 文本中的形状无关。

组形状中子形状的显示顺序由其在组形状内的 order 确定。

## 例子

展示如何操纵形状的顺序。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入三个不同颜色的矩形，彼此部分重叠。
// 当我们插入一个与另一个形状重叠的形状时，Aspose.Words 会将新形状放在旧形状之上。
// 浅绿色矩形将与浅蓝色矩形重叠并部分遮挡它，
// 浅蓝色矩形将遮挡橙色矩形。
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// 形状的“ZOrder”属性决定其在其他重叠形状中的堆叠优先级。
// 如果两个重叠形状具有不同的“ZOrder”值，
// Microsoft Word 会将具有较高值的形状放置在具有较低值的形状之上。 
// 设置形状的“ZOrder”值，将第一个橙色矩形放在第二个浅蓝色矩形之上
// 以及第三个浅绿色矩形上方的第二个浅蓝色矩形。
// 这将颠倒它们原来的堆叠顺序。
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
