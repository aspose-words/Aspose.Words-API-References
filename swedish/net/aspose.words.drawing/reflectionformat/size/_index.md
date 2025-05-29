---
title: ReflectionFormat.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ReflectionFormat Size, kontrollera reflektionsstorleken (0,0-1,0) för fantastiska visuella effekter i dina designer. Förbättra ditt projekts estetik!
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/reflectionformat/size/
---
## ReflectionFormat.Size property

Hämtar eller ställer in ett dubbelvärde mellan 0,0 och 1,0 som representerar storleken på reflektionen som en procentandel av det reflekterade objektet. Standardvärdet är 0,0.

```csharp
public double Size { get; set; }
```

## Exempel

Visar hur man interagerar med reflektionsformseffekten.

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

### Se även

* class [ReflectionFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
