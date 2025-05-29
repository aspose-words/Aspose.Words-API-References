---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ReflectionFormat 类，实现高级对象反射格式化。无缝集成，提升您的文档设计体验！
type: docs
weight: 1570
url: /zh/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

表示对象的反射格式。

```csharp
public class ReflectionFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | 获取或设置一个双精度值，以点为单位指定应用于反射效果的模糊效果程度。 默认值为 0.0。 |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | 获取或设置一个双精度值，以点为单位指定反射图像与对象的分离量。 默认值为 0.0。 |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | 获取或设置介于 0.0 和 1.0 之间的双精度值，表示反射的大小 占反射对象的百分比。 默认值为 0.0。 |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | 获取或设置介于 0.0（不透明）和 1.0（透明）之间的双精度值，表示反射效果的透明度。 默认值为 0.0。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | 删除`ReflectionFormat`来自父对象。 |

## 评论

使用[`Reflection`](../shapebase/reflection/)属性来访问对象的反射属性。 您不创建`ReflectionFormat`直接上课。

## 例子

展示如何与反射形状效果进行交互。

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
