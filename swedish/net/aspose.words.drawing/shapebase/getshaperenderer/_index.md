---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase GetShapeRenderer-metoden för att enkelt skapa och rendera former som bilder, vilket enkelt förbättrar dina designprojekt.
type: docs
weight: 670
url: /sv/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Skapar och returnerar ett objekt som kan användas för att rendera denna form till en bild.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Returvärde

Renderer-objektet för den här formen.

## Anmärkningar

Den här metoden anropar bara[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) konstruktorn och skickar detta objekt som en parameter.

## Exempel

Visar hur man använder en formrendering för att exportera former till filer i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Det finns 7 former i dokumentet, inklusive en gruppform med 2 underformer.
// Vi kommer att rendera varje form till en bildfil i det lokala filsystemet
// samtidigt som gruppformerna ignoreras eftersom de inte har något utseende.
// Detta kommer att producera 6 bildfiler.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Se även

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
