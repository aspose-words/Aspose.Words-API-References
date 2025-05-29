---
title: ImageSize.WidthPoints
linktitle: WidthPoints
articleTitle: WidthPoints
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageSize WidthPoints-Eigenschaft, um einfach die Bildbreite in Punkten zu ermitteln – perfekt für präzise Messungen in Designprojekten!
type: docs
weight: 70
url: /de/net/aspose.words.drawing/imagesize/widthpoints/
---
## ImageSize.WidthPoints property

Ruft die Breite des Bildes in Punkten ab. 1 Punkt entspricht 1/72 Zoll.

```csharp
public double WidthPoints { get; }
```

## Beispiele

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

* class [ImageSize](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
