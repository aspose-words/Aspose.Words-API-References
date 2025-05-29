---
title: ArrowLength Enum
linktitle: ArrowLength
articleTitle: ArrowLength
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ArrowLength 枚举，自定义箭头长度，增强文档中的线条图形效果。立即提升您的设计！
type: docs
weight: 720
url: /zh/net/aspose.words.drawing/arrowlength/
---
## ArrowLength enumeration

线末端箭头的长度。

```csharp
public enum ArrowLength
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Short | `0` |  |
| Medium | `1` |  |
| Long | `2` |  |
| Default | `0` | 相同Short. |

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

* property [StartArrowLength](../stroke/startarrowlength/)
* property [EndArrowLength](../stroke/endarrowlength/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
