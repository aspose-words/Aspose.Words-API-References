---
title: ReflectionFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words per .NET
description: Regola la trasparenza di ReflectionFormat da 0,0 (opaco) a 1,0 (trasparente) per effetti di riflessione personalizzabili. Migliora i tuoi progetti con precisione!
type: docs
weight: 40
url: /it/net/aspose.words.drawing/reflectionformat/transparency/
---
## ReflectionFormat.Transparency property

Ottiene o imposta un valore double compreso tra 0,0 (opaco) e 1,0 (trasparente) che rappresenta il grado di trasparenza per l'effetto di riflessione. Il valore predefinito è 0,0.

```csharp
public double Transparency { get; set; }
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

* class [ReflectionFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
