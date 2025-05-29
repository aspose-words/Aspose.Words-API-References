---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Drawing.GlowFormat för att förbättra dina dokument med fantastiska glödeffekter. Förhöj din design med unika formateringsalternativ!
type: docs
weight: 1300
url: /sv/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

Representerar glödformateringen för ett objekt.

```csharp
public class GlowFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | Hämtar eller ställer in enColor objekt som representerar färgen för en glödeffekt. Standardvärdet ärBlack . |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som representerar längden på radien för en glödeffekt i punkter (pt). Standardvärdet är 0,0. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | Hämtar eller ställer in graden av transparens för glödeffekten som ett värde mellan 0,0 (ogenomskinlig) och 1,0 (klar). Standardvärdet är 0,0. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | Tar bort`GlowFormat` från föräldraobjektet. |

## Anmärkningar

Använd[`Glow`](../shapebase/glow/) egenskap för att komma åt glödegenskaper för ett objekt. Du skapar inte instanser av`GlowFormat` klass direkt.

## Exempel

Visar hur man interagerar med glödformseffekten.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
