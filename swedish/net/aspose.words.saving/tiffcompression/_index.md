---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TiffCompression-uppräkningen för optimal sparning av TIFF-filer. Välj enkelt den bästa komprimeringstypen för högkvalitativa sidbilder.
type: docs
weight: 6430
url: /sv/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Anger vilken typ av komprimering som ska tillämpas när sidbilder sparas i en TIFF-fil.

```csharp
public enum TiffCompression
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Anger ingen komprimering. |
| Rle | `1` | Anger RLE-komprimeringsschemat. |
| Lzw | `2` | Anger LZW-komprimeringsschemat. I Java emuleras det av Deflate (Zip)-komprimering. |
| Ccitt3 | `3` | Anger CCITT3-komprimeringsschemat. |
| Ccitt4 | `4` | Anger CCITT4-komprimeringsschemat. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
