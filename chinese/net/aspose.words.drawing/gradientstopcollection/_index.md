---
title: GradientStopCollection Class
linktitle: GradientStopCollection
articleTitle: GradientStopCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.GradientStopCollection 班级. 包含以下集合GradientStop对象 在 C#.
type: docs
weight: 990
url: /zh/net/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class

包含以下集合[`GradientStop`](../gradientstop/)对象.

要了解更多信息，请访问[使用图形元素](https://docs.aspose.com/words/net/working-with-graphic-elements/)文档文章。

```csharp
public class GradientStopCollection : IEnumerable<GradientStop>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.drawing/gradientstopcollection/count/) { get; } | 获取一个整数值，指示集合中的项目数。 |
| [Item](../../aspose.words.drawing/gradientstopcollection/item/) { get; set; } | 获取或设置[`GradientStop`](../gradientstop/)集合中的对象. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.drawing/gradientstopcollection/add/)(*[GradientStop](../gradientstop/)*) | 添加指定的[`GradientStop`](../gradientstop/)到梯度. |
| [GetEnumerator](../../aspose.words.drawing/gradientstopcollection/getenumerator/)() | 返回一个迭代集合的枚举器。 |
| [Insert](../../aspose.words.drawing/gradientstopcollection/insert/)(*int, [GradientStop](../gradientstop/)*) | 插入一个[`GradientStop`](../gradientstop/)到指定索引处的集合。 |
| [Remove](../../aspose.words.drawing/gradientstopcollection/remove/)(*[GradientStop](../gradientstop/)*) | 删除指定的[`GradientStop`](../gradientstop/)来自集合. |
| [RemoveAt](../../aspose.words.drawing/gradientstopcollection/removeat/)(*int*) | 删除一个[`GradientStop`](../gradientstop/)来自指定索引处的集合。 |

## 评论

您不直接创建此类的实例。 使用[`GradientStops`](../fill/gradientstops/)用于访问填充对象的渐变停止点的属性。

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

* class [GradientStop](../gradientstop/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
