---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words för .NET
description: Optimera dina TIFF-bilder med egenskapen TiffCompression i ImageSaveOptions, så att du kan välja den bästa komprimeringsmetoden för kvalitetsresultat.
type: docs
weight: 180
url: /sv/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Hämtar eller ställer in vilken typ av komprimering som ska tillämpas när genererade bilder sparas i TIFF-format.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Anmärkningar

Gäller endast när man sparar till TIFF.

Standardvärdet ärLzw.

## Exempel

Visar hur man väljer komprimeringsschemat som ska tillämpas på ett dokument som vi konverterar till en TIFF-bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// Ställ in egenskapen "TiffCompression" till "TiffCompression.None" för att inte tillämpa någon komprimering vid sparning,
// vilket kan resultera i en mycket stor utdatafil.
// Ställ in egenskapen "TiffCompression" till "TiffCompression.Rle" för att tillämpa RLE-komprimering
// Sätt egenskapen "TiffCompression" till "TiffCompression.Lzw" för att tillämpa LZW-komprimering.
// Sätt egenskapen "TiffCompression" till "TiffCompression.Ccitt3" för att tillämpa CCITT3-komprimering.
// Sätt egenskapen "TiffCompression" till "TiffCompression.Ccitt4" för att tillämpa CCITT4-komprimering.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### Se även

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
