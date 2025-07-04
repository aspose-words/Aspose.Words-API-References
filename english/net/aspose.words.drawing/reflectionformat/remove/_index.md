---
title: ReflectionFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Effortlessly eliminate ReflectionFormat from your parent object with our streamlined Remove method, enhancing your coding efficiency and clarity.
type: docs
weight: 50
url: /net/aspose.words.drawing/reflectionformat/remove/
---
## ReflectionFormat.Remove method

Removes [`ReflectionFormat`](../) from the parent object.

```csharp
public void Remove()
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

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.That(reflectionFormat.Transparency, Is.EqualTo(0.37d).Within(0.01d));
Assert.That(reflectionFormat.Size, Is.EqualTo(0.48d).Within(0.01d));
Assert.That(reflectionFormat.Blur, Is.EqualTo(17.5d).Within(0.01d));
Assert.That(reflectionFormat.Distance, Is.EqualTo(9.2d).Within(0.01d));

reflectionFormat.Remove();

Assert.That(reflectionFormat.Transparency, Is.EqualTo(0));
Assert.That(reflectionFormat.Size, Is.EqualTo(0));
Assert.That(reflectionFormat.Blur, Is.EqualTo(0));
Assert.That(reflectionFormat.Distance, Is.EqualTo(0));
```

### See Also

* class [ReflectionFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
