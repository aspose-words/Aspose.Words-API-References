---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.ReflectionFormat för avancerad formatering av objektreflektion. Förbättra din dokumentdesign med sömlös integration!
type: docs
weight: 1570
url: /sv/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

Representerar reflektionsformateringen för ett objekt.

```csharp
public class ReflectionFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som anger graden av oskärpa som tillämpas på reflektionseffekten i punkter. Standardvärdet är 0,0. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som anger avståndet mellan den reflekterade bilden och objektet i punkter. Standardvärdet är 0,0. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | Hämtar eller ställer in ett dubbelvärde mellan 0,0 och 1,0 som representerar storleken på reflektionen som en procentandel av det reflekterade objektet. Standardvärdet är 0,0. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | Hämtar eller ställer in ett dubbelvärde mellan 0,0 (ogenomskinlig) och 1,0 (klar) som representerar graden av transparens för reflektionseffekten. Standardvärdet är 0,0. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | Tar bort`ReflectionFormat` från föräldraobjektet. |

## Anmärkningar

Använd[`Reflection`](../shapebase/reflection/) egenskap för att komma åt reflektionsegenskaper för ett objekt. Du skapar inte instanser av`ReflectionFormat` klass direkt.

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
