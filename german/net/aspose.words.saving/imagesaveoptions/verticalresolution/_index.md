---
title: ImageSaveOptions.VerticalResolution
linktitle: VerticalResolution
articleTitle: VerticalResolution
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ImageSaveOptions VerticalResolution“, um die Bildqualität in DPI einfach einzustellen und zu optimieren und so beeindruckende Bilder zu erzielen. Verbessern Sie Ihre Projekte noch heute!
type: docs
weight: 200
url: /de/net/aspose.words.saving/imagesaveoptions/verticalresolution/
---
## ImageSaveOptions.VerticalResolution property

Ruft die vertikale Auflösung für die generierten Bilder in Punkten pro Zoll ab oder legt sie fest.

```csharp
public float VerticalResolution { get; set; }
```

## Bemerkungen

Diese Eigenschaft wirkt sich nur beim Speichern in Rasterbildformaten aus und beeinflusst die Ausgabegröße in Pixeln.

Der Standardwert ist 96.

## Beispiele

Zeigt, wie das Bild bearbeitet wird, während Aspose.Words ein Dokument in eins konvertiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben an
// Bearbeiten Sie das Bild, während der Speichervorgang es rendert.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Wir können diese Eigenschaften anpassen, um die Helligkeit und den Kontrast des Bildes zu ändern.
    // Beide liegen auf einer Skala von 0 bis 1 und sind standardmäßig auf 0,5 eingestellt.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Mit diesen Eigenschaften können wir die horizontale und vertikale Auflösung anpassen.
    // Dies wirkt sich auf die Abmessungen des Bildes aus.
    // Der Standardwert für diese Eigenschaften ist 96,0, für eine Auflösung von 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Mit dieser Eigenschaft können wir das Bild skalieren. Der Standardwert ist 1,0, was einer Skalierung von 100 % entspricht.
    // Wir können diese Eigenschaft verwenden, um alle Änderungen der Bildabmessungen zu negieren, die durch eine Änderung der Auflösung verursacht würden.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
