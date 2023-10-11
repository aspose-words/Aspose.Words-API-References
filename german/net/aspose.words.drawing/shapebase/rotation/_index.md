---
title: ShapeBase.Rotation
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Definiert den Winkel in Grad um den eine Form gedreht wird. Positiver Wert entspricht dem Drehwinkel im Uhrzeigersinn.
type: docs
weight: 470
url: /de/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Definiert den Winkel (in Grad), um den eine Form gedreht wird. Positiver Wert entspricht dem Drehwinkel im Uhrzeigersinn.

```csharp
public double Rotation { get; set; }
```

### Bemerkungen

Der Standardwert ist 0.

### Beispiele

Zeigt, wie man ein Bild einfügt und dreht.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Form mit einem Bild einfügen.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Das Bild um 45 Grad im Uhrzeigersinn drehen.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


