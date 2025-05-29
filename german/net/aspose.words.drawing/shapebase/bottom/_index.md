---
title: ShapeBase.Bottom
linktitle: Bottom
articleTitle: Bottom
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase Bottom-Eigenschaft, um einfach auf die Position der unteren Kante des Blocks zuzugreifen, der Ihre Form enthält, und so eine präzise Designkontrolle zu ermöglichen.
type: docs
weight: 60
url: /de/net/aspose.words.drawing/shapebase/bottom/
---
## ShapeBase.Bottom property

Ruft die Position der Unterkante des umschließenden Blocks der Form ab.

```csharp
public double Bottom { get; }
```

## Bemerkungen

Bei einer Form der obersten Ebene wird der Wert in Punkten angegeben und ist relativ zum Formanker.

Bei Formen in einer Gruppe liegt der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe vor.

## Beispiele

Zeigt, wie Sie ein schwebendes Bild einfügen und seine Position und Größe angeben.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Konfigurieren Sie die Eigenschaft „RelativeHorizontalPosition“ der Form, um den Wert der Eigenschaft „Left“ zu behandeln
    // als horizontaler Abstand der Form in Punkten von der linken Seite der Seite.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Setzen Sie den horizontalen Abstand der Form von der linken Seite der Seite auf 100.
shape.Left = 100;

// Verwenden Sie die Eigenschaft „RelativeVerticalPosition“ auf ähnliche Weise, um die Form 80pt unterhalb des oberen Seitenrands zu positionieren.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Legen Sie die Höhe der Form fest. Dadurch wird die Breite automatisch skaliert, um die Abmessungen beizubehalten.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Die Eigenschaften „Bottom“ und „Right“ enthalten die unteren und rechten Ränder des Bildes.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
