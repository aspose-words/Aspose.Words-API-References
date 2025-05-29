---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase Name för att enkelt hantera valfria formnamn, vilket förbättrar din designflexibilitet och projektorganisation.
type: docs
weight: 420
url: /sv/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Hämtar eller anger det valfria formnamnet.

```csharp
public string Name { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

Kan inte vara`null`, men kan vara en tom sträng.

## Exempel

Visar hur man använder en forms alternativa text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Vi kan komma åt alternativtexten för en form genom att högerklicka på den och sedan via "Formatera autofigur" -> "Alternativ text".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Spara dokumentet som HTML och ta sedan bort den länkade bilden som tillhör vår form.
// Webbläsaren som läser vår HTML kommer att visa alt-texten istället för den saknade bilden.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
