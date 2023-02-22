---
title: Enum ImagePixelFormat
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.ImagePixelFormat enum. Specifica il formato pixel per le immagini generate delle pagine del documento.
type: docs
weight: 4960
url: /it/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Specifica il formato pixel per le immagini generate delle pagine del documento.

```csharp
public enum ImagePixelFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 bit per pixel, RGB. |
| Format16BppRgb565 | `1` | 16 bit per pixel, RGB. |
| Format16BppArgb1555 | `2` | 16 bit per pixel, ARGB. |
| Format24BppRgb | `3` | 24 bit per pixel, RGB. |
| Format32BppRgb | `4` | 32 bit per pixel, RGB. |
| Format32BppArgb | `5` | 32 bit per pixel, ARGB. |
| Format32BppPArgb | `6` | 32 bit per pixel, ARGB, alfa premoltiplicato. |
| Format48BppRgb | `7` | 48 bit per pixel, RGB. |
| Format64BppArgb | `8` | 64 bit per pixel, ARGB. |
| Format64BppPArgb | `9` | 64 bit per pixel, ARGB, alfa premoltiplicato. |
| Format1bppIndexed | `10` | 1 bit per pixel, indicizzato. |

### Esempi

Mostra come selezionare una velocità bit per pixel con cui eseguire il rendering di un documento in un'immagine.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
            // seleziona un formato pixel per l'immagine che genererà l'operazione di salvataggio.
            // Varie velocità di bit per pixel influenzeranno la qualità e la dimensione del file dell'immagine generata.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.PixelFormat = imagePixelFormat;

            // Possiamo clonare le istanze di ImageSaveOptions.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


