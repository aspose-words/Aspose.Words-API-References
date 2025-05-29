---
title: ReflectionFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words for .NET
description: 将 ReflectionFormat 的透明度从 0.0（不透明）调整到 1.0（透明），即可自定义反射效果。精准提升您的设计！
type: docs
weight: 40
url: /zh/net/aspose.words.drawing/reflectionformat/transparency/
---
## ReflectionFormat.Transparency property

获取或设置介于 0.0（不透明）和 1.0（透明）之间的双精度值，表示反射效果的透明度。 默认值为 0.0。

```csharp
public double Transparency { get; set; }
```

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

* class [ReflectionFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
