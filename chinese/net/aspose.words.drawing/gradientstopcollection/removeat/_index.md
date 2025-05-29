---
title: GradientStopCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: 使用 RemoveAt 方法轻松管理您的 GradientStopCollection。轻松通过索引移除 GradientStops，简化设计控制。
type: docs
weight: 70
url: /zh/net/aspose.words.drawing/gradientstopcollection/removeat/
---
## GradientStopCollection.RemoveAt method

删除[`GradientStop`](../../gradientstop/)来自指定索引处的集合。

```csharp
public GradientStop RemoveAt(int index)
```

### 返回值

已移除[`GradientStop`](../../gradientstop/)。

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

* class [GradientStop](../../gradientstop/)
* class [GradientStopCollection](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
