---
title: ImageSaveOptions.ImageColorMode
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSaveOptions eigendom. Ruft den Farbmodus für die generierten Bilder ab oder legt diesen fest.
type: docs
weight: 50
url: /de/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Ruft den Farbmodus für die generierten Bilder ab oder legt diesen fest.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

### Bemerkungen

Diese Eigenschaft ist nur beim Speichern in Rasterbildformaten wirksam.

Der Standardwert istNone.

### Beispiele

Zeigt, wie beim Rendern von Dokumenten ein Farbmodus festgelegt wird.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt an übergeben
            // Wählen Sie einen Farbmodus für das Bild aus, das durch den Speichervorgang generiert wird.
            // Wenn wir die Eigenschaft „ImageColorMode“ auf „ImageColorMode.BlackAndWhite“ setzen,
            // Der Speichervorgang wendet beim Rendern des Dokuments eine Graustufen-Farbreduzierung an.
            // Wenn wir die Eigenschaft „ImageColorMode“ auf „ImageColorMode.Grayscale“ setzen,
            // Durch den Speichervorgang wird das Dokument in ein monochromes Bild umgewandelt.
            // Wenn wir die Eigenschaft „ImageColorMode“ auf „None“ setzen, wendet der Speichervorgang die Standardmethode an
            // und alle Farben des Dokuments im Ausgabebild beibehalten.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.ImageColorMode = imageColorMode;

            doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(120000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#endif
```

### Siehe auch

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions/)
* Montage [Aspose.Words](../../../)


