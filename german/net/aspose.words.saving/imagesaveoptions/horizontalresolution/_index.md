---
title: ImageSaveOptions.HorizontalResolution
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSaveOptions eigendom. Ruft die horizontale Auflösung für die generierten Bilder in Punkten pro Zoll ab oder legt diese fest.
type: docs
weight: 30
url: /de/net/aspose.words.saving/imagesaveoptions/horizontalresolution/
---
## ImageSaveOptions.HorizontalResolution property

Ruft die horizontale Auflösung für die generierten Bilder in Punkten pro Zoll ab oder legt diese fest.

```csharp
public float HorizontalResolution { get; set; }
```

### Bemerkungen

Diese Eigenschaft wirkt sich nur beim Speichern in Rasterbildformaten aus und wirkt sich auf die Ausgabegröße in Pixel aus.

Der Standardwert ist 96.

### Beispiele

Zeigt, wie das Bild bearbeitet wird, während Aspose.Words ein Dokument in ein Dokument konvertiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt an übergeben
// Bearbeiten Sie das Bild, während der Speichervorgang es rendert.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Wir können diese Eigenschaften anpassen, um die Helligkeit und den Kontrast des Bildes zu ändern.
    // Beide liegen auf einer Skala von 0-1 und liegen standardmäßig bei 0,5.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Mit diesen Eigenschaften können wir die horizontale und vertikale Auflösung anpassen.
    // Dies wirkt sich auf die Abmessungen des Bildes aus.
    // Der Standardwert für diese Eigenschaften ist 96,0 für eine Auflösung von 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Mit dieser Eigenschaft können wir das Bild skalieren. Der Standardwert ist 1,0 für eine Skalierung von 100 %.
    // Wir können diese Eigenschaft verwenden, um alle Änderungen der Bildabmessungen zu negieren, die eine Änderung der Auflösung verursachen würde.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions/)
* Montage [Aspose.Words](../../../)


