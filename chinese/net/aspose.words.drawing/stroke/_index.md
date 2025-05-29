---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Stroke 类，使用可自定义的笔触增强您的形状，轻松为您的文档添加专业风格。
type: docs
weight: 1720
url: /zh/net/aspose.words.drawing/stroke/
---
## Stroke class

定义形状的描边。

要了解更多信息，请访问[使用形状](https://docs.aspose.com/words/net/working-with-shapes/)文档文章。

```csharp
public class Stroke
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | 获取或设置笔触的背景颜色。 |
| [BackThemeColor](../../aspose.words.drawing/stroke/backthemecolor/) { get; set; } | 获取或设置代表描边背景颜色的 ThemeColor 对象。 |
| [BackTintAndShade](../../aspose.words.drawing/stroke/backtintandshade/) { get; set; } | 获取或设置使描边背景颜色变亮或变暗的双精度值。 |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } | 获取笔触的基本前景色，不带任何修饰符。 |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | 定义笔触的颜色。 |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | 定义笔触的第二种颜色。 |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | 指定笔触的点和虚线图案。 |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | 定义笔划末端的箭头长度。 |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | 定义笔画末端的箭头。 |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | 定义笔画末端的箭头宽度。 |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | 定义笔画末端的端点样式。 |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | 获取填充格式`Stroke`. |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | 获取或设置笔触的前景色。 |
| [ForeThemeColor](../../aspose.words.drawing/stroke/forethemecolor/) { get; set; } | 获取或设置代表描边前景色的 ThemeColor 对象。 |
| [ForeTintAndShade](../../aspose.words.drawing/stroke/foretintandshade/) { get; set; } | 获取或设置使描边前景色变亮或变暗的双精度值。 |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | 定义描边图像或图案填充的图像。 |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | 定义折线的连接样式。 |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | 定义笔触的线条样式。 |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | 定义路径是否将被描边。 |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | 定义笔触的透明度。有效范围为 0 到 1。 |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | 定义笔画起点的箭头长度。 |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | 定义笔画起点的箭头。 |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | 定义笔画起点的箭头宽度。 |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | 获取或设置介于 0.0（不透明）和 1.0（透明）之间的值，表示笔触的透明度。 |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | 获取或设置指示笔画是否可见的标志。 |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | 定义描边形状路径的画笔粗细（以点为单位）。 |

## 评论

使用[`Stroke`](../shape/stroke/)属性来访问形状的笔触属性。 您不创建`Stroke`直接上课。

## 例子

显示如何改变笔触属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// 基本形状，例如矩形，有两个可见部分。
// 1 - 填充，适用于形状轮廓内的区域：
shape.Fill.ForeColor = Color.White;

// 2 - 笔触，标记形状的轮廓：
// 修改此形状的笔触的各种属性。
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
