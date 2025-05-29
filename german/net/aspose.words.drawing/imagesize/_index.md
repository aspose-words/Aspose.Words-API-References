---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.ImageSize, Ihre Anlaufstelle für detaillierte Einblicke in Bildgröße und -auflösung zur Verbesserung der Dokumentqualität.
type: docs
weight: 1400
url: /de/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Enthält Informationen zu Bildgröße und Auflösung.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Bildern](https://docs.aspose.com/words/net/working-with-images/) Dokumentationsartikel.

```csharp
public class ImageSize
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ImageSize](imagesize/#constructor)(*int, int*) | Initialisiert Breite und Höhe auf die angegebenen Werte in Pixeln. Initialisiert die Auflösung auf 96 dpi. |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | Initialisiert Breite, Höhe und Auflösung auf die angegebenen Werte. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | Ruft die Höhe des Bildes in Pixeln ab. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | Ruft die Höhe des Bildes in Punkten ab. 1 Punkt entspricht 1/72 Zoll. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | Ruft die horizontale Auflösung in DPI ab. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | Ruft die vertikale Auflösung in DPI ab. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | Ruft die Breite des Bildes in Pixeln ab. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | Ruft die Breite des Bildes in Punkten ab. 1 Punkt entspricht 1/72 Zoll. |

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

* property [ImageSize](../imagedata/imagesize/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
