---
title: GradientStop.Position
second_title: Aspose.Words for .NET API 参考
description: GradientStop 财产. 获取或设置一个值表示梯度 内停止点的位置以 0.0 到 1.0 范围内的百分比表示
type: docs
weight: 40
url: /zh/net/aspose.words.drawing/gradientstop/position/
---
## GradientStop.Position property

获取或设置一个值，表示梯度 内停止点的位置，以 0.0 到 1.0 范围内的百分比表示。

```csharp
public double Position { get; set; }
```

### 例子

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

* class [GradientStop](../)
* 命名空间 [Aspose.Words.Drawing](../../gradientstop/)
* 部件 [Aspose.Words](../../../)


