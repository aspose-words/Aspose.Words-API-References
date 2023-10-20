---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.TiffCompression enum. Specifica il tipo di compressione da applicare quando si salvano le immagini della pagina in un file TIFF in C#.
type: docs
weight: 5630
url: /it/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Specifica il tipo di compressione da applicare quando si salvano le immagini della pagina in un file TIFF.

```csharp
public enum TiffCompression
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Non specifica alcuna compressione. |
| Rle | `1` | Specifica lo schema di compressione RLE. |
| Lzw | `2` | Specifica lo schema di compressione LZW. In Java emulato dalla compressione Deflate (Zip). |
| Ccitt3 | `3` | Specifica lo schema di compressione CCITT3. |
| Ccitt4 | `4` | Specifica lo schema di compressione CCITT4. |

## Esempi

Mostra come selezionare lo schema di compressione da applicare a un documento che convertiamo in un'immagine TIFF.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
            // per modificare il modo in cui il metodo trasforma il documento in un'immagine.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // Imposta la proprietà "TiffCompression" su "TiffCompression.None" per non applicare alcuna compressione durante il salvataggio,
            // il che potrebbe generare un file di output molto grande.
            // Imposta la proprietà "TiffCompression" su "TiffCompression.Rle" per applicare la compressione RLE
            // Imposta la proprietà "TiffCompression" su "TiffCompression.Lzw" per applicare la compressione LZW.
            // Imposta la proprietà "TiffCompression" su "TiffCompression.Ccitt3" per applicare la compressione CCITT3.
            // Imposta la proprietà "TiffCompression" su "TiffCompression.Ccitt4" per applicare la compressione CCITT4.
            options.TiffCompression = tiffCompression;

            doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);

            switch (tiffCompression)
            {
                case TiffCompression.None:
                    Assert.That(3000000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Rle:
#if NET5_0_OR_GREATER
                    Assert.That(6000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#else
                    Assert.That(600000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#endif
                    break;
                case TiffCompression.Lzw:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt3:
                    Assert.That(90000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt4:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
            }
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
