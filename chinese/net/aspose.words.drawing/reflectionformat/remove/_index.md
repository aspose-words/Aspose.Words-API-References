---
title: ReflectionFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 使用我们简化的 Remove 方法轻松地从父对象中消除 ReflectionFormat，从而提高您的编码效率和清晰度。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing/reflectionformat/remove/
---
## ReflectionFormat.Remove method

删除[`ReflectionFormat`](../)来自父对象。

```csharp
public void Remove()
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
