---
title: ShapeBase.Name
second_title: Aspose.Words för .NET API Referens
description: ShapeBase fast egendom. Hämtar eller ställer in det valfria formnamnet.
type: docs
weight: 400
url: /sv/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Hämtar eller ställer in det valfria formnamnet.

```csharp
public string Name { get; set; }
```

### Anmärkningar

Standard är tom sträng.

Kan inte vara`null`, men kan vara en tom sträng.

### Exempel

Visar hur man använder en forms alternativa text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Vi kan komma åt den alternativa texten i en form genom att högerklicka på den och sedan via "Formatera AutoShape" -> "Alt text".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Spara dokumentet i HTML och ta sedan bort den länkade bilden som tillhör vår form.
// Webbläsaren som läser vår HTML kommer att visa alt-texten i stället för den saknade bilden.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../shapebase/)
* hopsättning [Aspose.Words](../../../)


