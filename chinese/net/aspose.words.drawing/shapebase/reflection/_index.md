---
title: ShapeBase.Reflection
linktitle: Reflection
articleTitle: Reflection
second_title: Aspose.Words for .NET
description: 探索 ShapeBase 反射属性，通过可自定义的反射格式增强您的设计，获得令人惊叹的视觉效果。
type: docs
weight: 440
url: /zh/net/aspose.words.drawing/shapebase/reflection/
---
## ShapeBase.Reflection property

获取形状的反射格式。

```csharp
public ReflectionFormat Reflection { get; }
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

* class [ReflectionFormat](../../reflectionformat/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
