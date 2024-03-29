---
title: ArrowType Enum
linktitle: ArrowType
articleTitle: ArrowType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.ArrowType 枚举. 指定行末端箭头的类型 在 C#.
type: docs
weight: 490
url: /zh/net/aspose.words.drawing/arrowtype/
---
## ArrowType enumeration

指定行末端箭头的类型。

```csharp
public enum ArrowType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 该行末尾没有箭头。 |
| Arrow | `1` | 箭头是实心三角形。 |
| Stealth | `2` | 该箭头是“隐形”箭头。 |
| Diamond | `3` | 线端是实心菱形。 |
| Oval | `4` | 线端是实心椭圆形。 |
| Open | `5` | 箭头是空心箭头。 |
| Default | `0` | 与相同None. |

## 例子

展示创造出各种形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是我们可以插入到文档中的四个形状示例。
// 1 - 水平、半透明红点线
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

// 4 - 方向翻转的箭头，填充有 Aspose 徽标：
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
    // 在让形状显示它之前，以另一种方式翻转图像以取消此效果。
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### 也可以看看

* property [StartArrowType](../stroke/startarrowtype/)
* property [EndArrowType](../stroke/endarrowtype/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
