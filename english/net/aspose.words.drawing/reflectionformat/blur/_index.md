---
title: ReflectionFormat.Blur
linktitle: Blur
articleTitle: Blur
second_title: Aspose.Words for .NET
description: ReflectionFormat Blur property. Gets or sets a double value that specifies the degree of blur effect applied to the reflection effect in points. The default value is 0.0 in C#.
type: docs
weight: 10
url: /net/aspose.words.drawing/reflectionformat/blur/
---
## ReflectionFormat.Blur property

Gets or sets a double value that specifies the degree of blur effect applied to the reflection effect in points. The default value is 0.0.

```csharp
public double Blur { get; set; }
```

## Examples

Shows how to interact with reflection shape effect.

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

Assert.AreEqual(0.37d, shape.Reflection.Transparency, 0.01d);
Assert.AreEqual(0.48d, shape.Reflection.Size, 0.01d);
Assert.AreEqual(17.5d, shape.Reflection.Blur, 0.01d);
Assert.AreEqual(9.2d, shape.Reflection.Distance, 0.01d);

shape.Reflection.Remove();

Assert.AreEqual(0, shape.Reflection.Transparency);
Assert.AreEqual(0, shape.Reflection.Size);
Assert.AreEqual(0, shape.Reflection.Blur);
Assert.AreEqual(0, shape.Reflection.Distance);
```

### See Also

* class [ReflectionFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
