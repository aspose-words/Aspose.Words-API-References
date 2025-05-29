---
title: ShapeBase.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase Height-Eigenschaft, um die Containerhöhe Ihrer Form einfach anzupassen und so die Designflexibilität und Präzision Ihrer Projekte zu verbessern.
type: docs
weight: 210
url: /de/net/aspose.words.drawing/shapebase/height/
---
## ShapeBase.Height property

Ruft die Höhe des umgebenden Blocks der Form ab oder legt sie fest.

```csharp
public double Height { get; set; }
```

## Bemerkungen

Bei einer Form der obersten Ebene wird der Wert in Punkten angegeben.

Bei Formen in einer Gruppe liegt der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe vor.

Der Standardwert ist 0.

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

Zeigt, wie die Größe einer Form mit einem Bild geändert wird.

```csharp
// Wenn wir ein Bild mit der Methode "InsertImage" einfügen, skaliert der Builder die Form, die das Bild anzeigt, so dass
// Wenn wir das Dokument in Microsoft Word mit 100 % Zoom anzeigen, zeigt die Form das Bild in seiner tatsächlichen Größe an.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Ein 400 x 400 Bild erstellt ein ImageData-Objekt mit einer Bildgröße von 300 x 300 pt.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Wenn die Abmessungen einer Form mit den Abmessungen der Bilddaten übereinstimmen,
// dann zeigt die Form das Bild in seiner Originalgröße an.
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

    // Reduzieren Sie die Gesamtgröße der Form um 50 %.
shape.Width *= 0.5;

    // Skalierungsfaktoren gelten gleichzeitig für die Breite und die Höhe, um die Proportionen der Form beizubehalten.
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// Wenn wir die Größe der Form ändern, bleibt die Größe der Bilddaten gleich.
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Wir können auf die Abmessungen der Bilddaten verweisen, um eine Skalierung basierend auf der Größe des Bildes anzuwenden.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
