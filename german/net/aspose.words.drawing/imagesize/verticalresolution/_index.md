---
title: ImageSize.VerticalResolution
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSize eigendom. Ruft die vertikale Auflösung in DPI ab.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/imagesize/verticalresolution/
---
## ImageSize.VerticalResolution property

Ruft die vertikale Auflösung in DPI ab.

```csharp
public double VerticalResolution { get; }
```

### Beispiele

Zeigt, wie die Eigenschaften eines Bildes in einer Form gelesen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Form in das Dokument ein, die ein Bild aus unserem lokalen Dateisystem enthält.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn die Form ein Bild enthält, ist ihre ImageData-Eigenschaft gültig,
// und es enthält ein ImageSize-Objekt.
ImageSize imageSize = shape.ImageData.ImageSize; 

// Das ImageSize-Objekt enthält schreibgeschützte Informationen über das Bild innerhalb der Form.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// Wir können die Größe der Form auf der Größe ihres Bildes basieren, um ein Dehnen des Bildes zu vermeiden.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Siehe auch

* class [ImageSize](../)
* namensraum [Aspose.Words.Drawing](../../imagesize/)
* Montage [Aspose.Words](../../../)


