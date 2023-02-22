---
title: ImageSaveOptions.TiffCompression
second_title: Aspose.Words för .NET API Referens
description: ImageSaveOptions fast egendom. Hämtar eller ställer in vilken typ av komprimering som ska tillämpas när genererade bilder sparas i TIFFformatet.
type: docs
weight: 170
url: /sv/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Hämtar eller ställer in vilken typ av komprimering som ska tillämpas när genererade bilder sparas i TIFF-formatet.

```csharp
public TiffCompression TiffCompression { get; set; }
```

### Anmärkningar

Har endast effekt när du sparar till TIFF.

Standardvärdet ärLzw.

### Exempel

Visar hur man väljer det komprimeringsschema som ska tillämpas på ett dokument som vi konverterar till en TIFF-bild.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
            // för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // Ställ in egenskapen "TiffCompression" till "TiffCompression.None" för att inte tillämpa någon komprimering när du sparar,
            // vilket kan resultera i en mycket stor utdatafil.
            // Ställ in egenskapen "TiffCompression" till "TiffCompression.Rle" för att tillämpa RLE-komprimering
            // Ställ in egenskapen "TiffCompression" till "TiffCompression.Lzw" för att tillämpa LZW-komprimering.
            // Ställ in egenskapen "TiffCompression" till "TiffCompression.Ccitt3" för att tillämpa CCITT3-komprimering.
            // Ställ in egenskapen "TiffCompression" till "TiffCompression.Ccitt4" för att tillämpa CCITT4-komprimering.
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

### Se även

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../imagesaveoptions/)
* hopsättning [Aspose.Words](../../../)


