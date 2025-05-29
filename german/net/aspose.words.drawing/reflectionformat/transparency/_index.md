---
title: ReflectionFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words für .NET
description: Passen Sie die Transparenz des ReflectionFormats von 0,0 (undurchsichtig) bis 1,0 (transparent) an, um individuelle Reflexionseffekte zu erzielen. Verbessern Sie Ihre Designs mit Präzision!
type: docs
weight: 40
url: /de/net/aspose.words.drawing/reflectionformat/transparency/
---
## ReflectionFormat.Transparency property

Ruft einen Double-Wert zwischen 0,0 (undurchsichtig) und 1,0 (durchsichtig) ab oder legt ihn fest, der den Grad der Transparenz für den Reflexionseffekt darstellt. Der Standardwert ist 0,0.

```csharp
public double Transparency { get; set; }
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
