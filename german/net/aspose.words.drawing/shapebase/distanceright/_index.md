---
title: ShapeBase.DistanceRight
linktitle: DistanceRight
articleTitle: DistanceRight
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase DistanceRight-Eigenschaft und passen Sie den Abstand in Punkten zwischen Ihrem Dokumenttext und der rechten Kante einer Form einfach an, um die Layoutkontrolle zu verbessern.
type: docs
weight: 150
url: /de/net/aspose.words.drawing/shapebase/distanceright/
---
## ShapeBase.DistanceRight property

Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und dem rechten Rand der Form zurück oder legt ihn fest.

```csharp
public double DistanceRight { get; set; }
```

## Bemerkungen

Der Standardwert ist 1/8 Zoll.

Wirkt sich nur auf Formen der obersten Ebene aus.

## Beispiele

Zeigt, wie der Umbruchabstand für einen Text festgelegt wird, der eine Form umgibt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Rechteck ein und sorgen Sie dafür, dass der Text eng um seine Grenzen herum verläuft.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Legen Sie den Mindestabstand zwischen der Form und dem umgebenden Text auf 40pt von allen Seiten fest.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Verschieben Sie die Form näher an die Seitenmitte und drehen Sie die Form dann um 60 Grad im Uhrzeigersinn.
shape.Top = 75;
shape.Left = 150;
shape.Rotation = 60;

// Text hinzufügen, der um die Form herumläuft.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
