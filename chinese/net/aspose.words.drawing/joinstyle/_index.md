---
title: JoinStyle Enum
linktitle: JoinStyle
articleTitle: JoinStyle
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.JoinStyle 枚举，获取多种线连接样式。以专业的品质和灵活性增强您的文档图形。
type: docs
weight: 1420
url: /zh/net/aspose.words.drawing/joinstyle/
---
## JoinStyle enumeration

线连接样式。

```csharp
public enum JoinStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Bevel | `0` | 用直线连接边缘。 |
| Miter | `1` | 延伸边缘直到它们连接。 |
| Round | `2` | 在两条边之间画一条弧线。 |

## 例子

展现出多种多样的造型创造。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是我们可以插入到文档中的四个形状的示例。
// 1 - 虚线，水平，半透明红线
// 左端有一个箭头，右端有一个菱形：
Shape arrow = new Shape(doc, ShapeType.Line);
arrow.Width = 200;
arrow.Stroke.Color = Color.Red;
arrow.Stroke.StartArrowType = ArrowType.Arrow;
arrow.Stroke.StartArrowLength = ArrowLength.Long;
arrow.Stroke.StartArrowWidth = ArrowWidth.Wide;
arrow.Stroke.EndArrowType = ArrowType.Diamond;
arrow.Stroke.EndArrowLength = ArrowLength.Long;
arrow.Stroke.EndArrowWidth = ArrowWidth.Wide;
arrow.Stroke.DashStyle = DashStyle.Dash;
arrow.Stroke.Opacity = 0.5;

Assert.AreEqual(JoinStyle.Miter, arrow.Stroke.JoinStyle);

builder.InsertNode(arrow);

// 2 - 带有圆形末端的粗黑色对角线：
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - 绿色填充的箭头：
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - 翻转方向的箭头，填充 Aspose 徽标：
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // 当我们翻转箭头的方向时，我们也会翻转箭头包含的图像。
    // 在获得显示形状之前，将图像翻转到另一个方向以取消此操作。
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### 也可以看看

* property [JoinStyle](../stroke/joinstyle/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
