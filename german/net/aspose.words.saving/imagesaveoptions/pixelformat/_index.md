---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die PixelFormat-Eigenschaft von ImageSaveOptions, um das Pixelformat Ihrer generierten Bilder für optimale Qualität und Leistung einfach anzupassen.
type: docs
weight: 120
url: /de/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Ruft das Pixelformat für die generierten Bilder ab oder legt es fest.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Bemerkungen

Diese Eigenschaft wirkt sich nur beim Speichern in Rasterbildformaten aus.

Der Standardwert istFormat32BppArgb.

Das Pixelformat des Ausgabebildes kann aufgrund der Arbeit von GDI+ vom eingestellten Wert abweichen.

## Beispiele

Zeigt, wie Sie eine Bit-pro-Pixel-Rate auswählen, mit der ein Dokument in ein Bild gerendert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben an
// Wählen Sie ein Pixelformat für das Bild aus, das beim Speichern generiert wird.
// Verschiedene Bit-pro-Pixel-Raten wirken sich auf die Qualität und Dateigröße des generierten Bildes aus.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Wir können ImageSaveOptions-Instanzen klonen.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Siehe auch

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
