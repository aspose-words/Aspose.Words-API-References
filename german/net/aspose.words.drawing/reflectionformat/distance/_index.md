---
title: ReflectionFormat.Distance
linktitle: Distance
articleTitle: Distance
second_title: Aspose.Words für .NET
description: Entdecken Sie die ReflectionFormat-Distanzeigenschaft. Passen Sie den Abstand Ihres reflektierten Bildes in Punkten einfach an, um beeindruckende visuelle Effekte zu erzielen. Der Standardwert ist 0,0.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/reflectionformat/distance/
---
## ReflectionFormat.Distance property

Ruft einen Double-Wert ab oder legt ihn fest, der den Abstand des reflektierten Bilds vom Objekt in Punkten angibt. Der Standardwert ist 0,0.

```csharp
public double Distance { get; set; }
```

## Beispiele

Zeigt, wie mit dem Reflexionsformeffekt interagiert wird.

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

### Siehe auch

* class [ReflectionFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
