---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase GetShapeRenderer-Methode, um mühelos Formen als Bilder zu erstellen und zu rendern und so Ihre Designprojekte problemlos zu verbessern.
type: docs
weight: 670
url: /de/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Erstellt und gibt ein Objekt zurück, mit dem diese Form in ein Bild gerendert werden kann.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Rückgabewert

Das Rendererobjekt für diese Form.

## Bemerkungen

Diese Methode ruft lediglich die[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) Konstruktor und übergibt dieses Objekt als Parameter.

## Beispiele

Zeigt, wie Sie mit einem Formrenderer Formen in Dateien im lokalen Dateisystem exportieren.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Das Dokument enthält 7 Formen, darunter eine Gruppenform mit 2 untergeordneten Formen.
// Wir rendern jede Form in eine Bilddatei im lokalen Dateisystem
// wobei die Gruppenformen ignoriert werden, da sie nicht angezeigt werden.
// Dadurch werden 6 Bilddateien erstellt.
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
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
