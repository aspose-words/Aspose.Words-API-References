---
title: ShapeBase.GetShapeRenderer
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase methode. Erstellt ein Objekt und gibt es zurück das zum Rendern dieser Form in ein Bild verwendet werden kann.
type: docs
weight: 660
url: /de/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Erstellt ein Objekt und gibt es zurück, das zum Rendern dieser Form in ein Bild verwendet werden kann.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Rückgabewert

Das Renderer-Objekt für diese Form.

### Bemerkungen

Diese Methode ruft lediglich die auf[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) Konstruktor und übergibt dieses Objekt als Parameter.

### Beispiele

Zeigt, wie Sie mit einem Formrenderer Formen in Dateien im lokalen Dateisystem exportieren.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Das Dokument enthält 7 Formen, darunter eine Gruppenform mit zwei untergeordneten Formen.
// Wir rendern jede Form in eine Bilddatei im lokalen Dateisystem
// während die Gruppenformen ignoriert werden, da sie kein Aussehen haben.
// Dies erzeugt 6 Bilddateien.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Siehe auch

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


