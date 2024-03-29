---
title: ShapeBase.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words für .NET
description: ShapeBase DistanceBottom eigendom. Gibt den Abstand in Punkten zwischen dem Dokumenttext und der Unterkante der Form zurück oder legt ihn fest in C#.
type: docs
weight: 130
url: /de/net/aspose.words.drawing/shapebase/distancebottom/
---
## ShapeBase.DistanceBottom property

Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und der Unterkante der Form zurück oder legt ihn fest.

```csharp
public double DistanceBottom { get; set; }
```

## Bemerkungen

Der Standardwert ist 0.

Hat nur Auswirkungen auf Formen der obersten Ebene.

## Beispiele

Zeigt, wie der Umbruchabstand für einen Text festgelegt wird, der eine Form umgibt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Füge ein Rechteck ein und sorge dafür, dass der Text seine Grenzen eng umschließt.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Stellen Sie den Mindestabstand zwischen der Form und dem umgebenden Text von allen Seiten auf 40 pt ein.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Verschieben Sie die Form näher an die Mitte der Seite und drehen Sie die Form dann um 60 Grad im Uhrzeigersinn.
shape.Top = 75;
shape.Left = 150; 
shape.Rotation = 60;

// Text hinzufügen, der die Form umschließt.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
