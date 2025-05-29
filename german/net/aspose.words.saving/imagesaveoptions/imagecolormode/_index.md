---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageColorMode-Eigenschaft von ImageSaveOptions, um den Farbmodus für Ihre generierten Bilder einfach anzupassen und zu optimieren. Verbessern Sie Ihre Visualisierungen noch heute!
type: docs
weight: 50
url: /de/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Ruft den Farbmodus für die generierten Bilder ab oder legt ihn fest.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## Bemerkungen

Diese Eigenschaft wirkt sich nur beim Speichern in Rasterbildformaten aus.

Der Standardwert istNone.

## Beispiele

Zeigt, wie beim Rendern von Dokumenten ein Farbmodus festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben an
// Wählen Sie einen Farbmodus für das Bild aus, das beim Speichern generiert wird.
// Wenn wir die Eigenschaft "ImageColorMode" auf "ImageColorMode.BlackAndWhite" setzen,
// Beim Speichern wird beim Rendern des Dokuments eine Graustufenfarbreduzierung angewendet.
    // Wenn wir die Eigenschaft "ImageColorMode" auf "ImageColorMode.Grayscale" setzen,
// Durch den Speichervorgang wird das Dokument in ein monochromes Bild umgewandelt.
// Wenn wir die Eigenschaft „ImageColorMode“ auf „None“ setzen, wird beim Speichern die Standardmethode angewendet
// und alle Farben des Dokuments im Ausgabebild beibehalten.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Siehe auch

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
