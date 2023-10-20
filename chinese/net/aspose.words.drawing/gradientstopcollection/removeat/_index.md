---
title: GradientStopCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: 用于 .NET 的 Aspose.Words
description: GradientStopCollection RemoveAt 方法. 删除一个GradientStop来自指定索引处的集合 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.drawing/gradientstopcollection/removeat/
---
## GradientStopCollection.RemoveAt method

删除一个[`GradientStop`](../../gradientstop/)来自指定索引处的集合。

```csharp
public GradientStop RemoveAt(int index)
```

### 返回值

已删除[`GradientStop`](../../gradientstop/)。

## 例子

演示如何向渐变填充添加渐变停止点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// 获取梯度停止集合。
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// 更改第一个梯度停止点。            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// 将新的梯度停止点添加到集合的末尾。
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// 删除索引 1 处的梯度停止点。
gradientStops.RemoveAt(1);
// 并在同一索引 1 处插入新的梯度停止点。
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// 删除集合中最后一个梯度停止点。
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

// 使用compliance选项通过DML定义形状
// 如果你想在文档保存后获取“GradientStops”属性。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### 也可以看看

* class [GradientStop](../../gradientstop/)
* class [GradientStopCollection](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
