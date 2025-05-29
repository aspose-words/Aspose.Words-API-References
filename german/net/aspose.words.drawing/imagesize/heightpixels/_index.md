---
title: ImageSize.HeightPixels
linktitle: HeightPixels
articleTitle: HeightPixels
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageSize HeightPixels-Eigenschaft, um einfach auf die Höhe Ihres Bilds in Pixeln zuzugreifen und diese für eine bessere Leistung und Qualität zu optimieren.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/imagesize/heightpixels/
---
## ImageSize.HeightPixels property

Ruft die Höhe des Bildes in Pixeln ab.

```csharp
public int HeightPixels { get; }
```

## Beispiele

Zeigt, wie die Eigenschaften eines Bildes in einer Form gelesen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Form in das Dokument ein, die ein Bild aus unserem lokalen Dateisystem enthält.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn die Form ein Bild enthält, ist ihre ImageData-Eigenschaft gültig.
// und es wird ein ImageSize-Objekt enthalten.
ImageSize imageSize = shape.ImageData.ImageSize;

// Das ImageSize-Objekt enthält schreibgeschützte Informationen über das Bild innerhalb der Form.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// Wir können die Größe der Form auf der Größe ihres Bildes basieren, um eine Streckung des Bildes zu vermeiden.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Siehe auch

* class [ImageSize](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
