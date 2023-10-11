---
title: Enum DashStyle
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.DashStyle 枚举. 虚线样式
type: docs
weight: 930
url: /zh/net/aspose.words.drawing/dashstyle/
---
## DashStyle enumeration

虚线样式。

```csharp
public enum DashStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Solid | `0` | 实心（连续）笔。 |
| ShortDash | `1` | 系统破折号样式。 |
| ShortDot | `2` | 系统破折号样式。 |
| ShortDashDot | `3` | 系统破折号样式。 |
| ShortDashDotDot | `4` | 系统破折号样式。 |
| Dot | `5` | 方点样式。 |
| Dash | `6` | 破折号样式。 |
| LongDash | `7` | 长破折号样式。 |
| DashDot | `8` | 短划线。 |
| LongDashDot | `9` | 长划线 短划线. |
| LongDashDotDot | `10` | 长划线 短划线 短划线. |
| Default | `0` | 与相同Solid. |

### 例子

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

* property [DashStyle](../stroke/dashstyle/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)


