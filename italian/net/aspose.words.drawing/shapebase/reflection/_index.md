---
title: ShapeBase.Reflection
linktitle: Reflection
articleTitle: Reflection
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase Reflection per migliorare i tuoi progetti con una formattazione personalizzabile dei riflessi, per effetti visivi sorprendenti.
type: docs
weight: 440
url: /it/net/aspose.words.drawing/shapebase/reflection/
---
## ShapeBase.Reflection property

Ottiene la formattazione della riflessione per la forma.

```csharp
public ReflectionFormat Reflection { get; }
```

## Esempi

Mostra come interagire con l'effetto forma riflesso.

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

### Guarda anche

* class [ReflectionFormat](../../reflectionformat/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
