---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Rotationseigenschaft, definieren und passen Sie Rotationswinkel für Ihre Formen einfach an und verbessern Sie so die Präzision und Kreativität Ihres Designs.
type: docs
weight: 500
url: /de/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Definiert den Winkel (in Grad), um den eine Form gedreht wird. Ein positiver Wert entspricht einem Drehwinkel im Uhrzeigersinn.

```csharp
public double Rotation { get; set; }
```

## Bemerkungen

Der Standardwert ist 0.

## Beispiele

Zeigt, wie man ein Bild einfügt und dreht.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Form mit einem Bild ein.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Drehen Sie das Bild um 45 Grad im Uhrzeigersinn.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
