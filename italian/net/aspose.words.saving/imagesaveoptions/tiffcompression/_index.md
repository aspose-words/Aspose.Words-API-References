---
title: ImageSaveOptions.TiffCompression
second_title: Aspose.Words per .NET API Reference
description: ImageSaveOptions proprietà. Ottiene o imposta il tipo di compressione da applicare quando si salvano le immagini generate nel formato TIFF.
type: docs
weight: 180
url: /it/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Ottiene o imposta il tipo di compressione da applicare quando si salvano le immagini generate nel formato TIFF.

```csharp
public TiffCompression TiffCompression { get; set; }
```

### Osservazioni

Ha effetto solo quando si salva in TIFF.

Il valore predefinito èLzw.

### Esempi

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

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../imagesaveoptions/)
* assemblea [Aspose.Words](../../../)


