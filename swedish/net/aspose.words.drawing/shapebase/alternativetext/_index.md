---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase AlternativeText-egenskapen, som förbättrar tillgängligheten genom att ge beskrivande text för grafik, vilket förbättrar användarupplevelsen och SEO.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Definierar alternativ text som ska visas istället för grafik.

```csharp
public string AlternativeText { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

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
