---
title: ImageSaveOptions.Clone
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSaveOptions methode. Erstellt einen tiefen Klon dieses Objekts.
type: docs
weight: 200
url: /de/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

Erstellt einen tiefen Klon dieses Objekts.

```csharp
public ImageSaveOptions Clone()
```

### Beispiele

Zeigt, wie Sie eine Bit-pro-Pixel-Rate auswählen, mit der ein Dokument in ein Bild gerendert wird.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt an übergeben
            // Wählen Sie ein Pixelformat für das Bild aus, das der Speichervorgang generiert.
            // Verschiedene Bit-pro-Pixel-Raten wirken sich auf die Qualität und Dateigröße des generierten Bildes aus.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.PixelFormat = imagePixelFormat;

            // Wir können ImageSaveOptions-Instanzen klonen.
            Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

            doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format32BppRgb:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(70000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                case ImagePixelFormat.Format32BppRgb:
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#endif
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions/)
* Montage [Aspose.Words](../../../)


