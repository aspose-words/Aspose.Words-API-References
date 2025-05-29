---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Bilder mit der FitImageToShape-Methode und sorgen Sie für eine perfekte Ausrichtung des Seitenverhältnisses innerhalb der Shape-Rahmen für beeindruckende visuelle Präsentationen.
type: docs
weight: 190
url: /de/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

Passt die Bilddaten an den Formrahmen an, sodass das Seitenverhältnis der Bilddaten dem Seitenverhältnis des Formrahmens entspricht.

```csharp
public void FitImageToShape()
```

## Beispiele

Zeigt, wie die Bilddaten in den Formrahmen eingepasst werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Bildform ein und belassen Sie ihre Ausrichtung im Standardzustand.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### Siehe auch

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
