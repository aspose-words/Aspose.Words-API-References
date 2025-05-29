---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.GradientStop 类，它是您创建令人惊叹的渐变并具有可自定义停止点以增强文档视觉效果的解决方案。
type: docs
weight: 1310
url: /zh/net/aspose.words.drawing/gradientstop/
---
## GradientStop class

表示一个渐变停止点。

要了解更多信息，请访问[使用图形元素](https://docs.aspose.com/words/net/working-with-graphic-elements/)文档文章。

```csharp
public class GradientStop
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | 初始化`GradientStop`类. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | 初始化`GradientStop`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | 获取表示渐变停止颜色的值，不带任何修饰符。 |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | 获取或设置表示渐变停止颜色的值。 |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | 获取或设置表示渐变内停止位置的值 以 0.0 到 1.0 范围内的百分比表示。 |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | 获取或设置表示渐变填充透明度的值 以 0.0 到 1.0 范围内的百分比表示。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | 从父级中删除渐变停止[`GradientStopCollection`](../gradientstopcollection/). |

## 例子

展示如何将渐变停止点添加到渐变填充。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// 获取渐变停止点集合。
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// 改变第一个梯度停止点。
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// 将新的渐变停止点添加到集合的末尾。
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// 移除索引 1 处的渐变停止点。
gradientStops.RemoveAt(1);
// 并在相同的索引 1 处插入新的渐变停止点。
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// 删除集合中的最后一个渐变停止点。
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// 使用合规性选项通过 DML 定义形状
// 如果您想在文档保存后获取“GradientStops”属性。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
