---
title: Enum ImageType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.ImageType uppräkning. Anger typen formatet av en bild i ett Microsoft Worddokument.
type: docs
weight: 1080
url: /sv/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Anger typen (formatet) av en bild i ett Microsoft Word-dokument.

```csharp
public enum ImageType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| NoImage | `0` | Det finns inga bilddata. |
| Unknown | `1` | En okänd bildtyp eller bildtyp som inte kan lagras direkt i ett Microsoft Word-dokument. |
| Emf | `2` | Windows Enhanced Metafile. |
| Wmf | `3` | Windows-metafil. |
| Pict | `4` | Macintosh PICT. En befintlig bild kommer att bevaras i ett dokument, men det stöds inte att infoga new PICT-bilder i ett dokument. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Portabel nätverksgrafik. |
| Bmp | `7` | Windows Bitmap. |
| Eps | `8` | Encapsulated PostScript. |

### Exempel

Visar hur man lägger till en bild i en form och kontrollerar dess typ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // Bilden i URL:en är en .gif. Om du infogar det i ett dokument omvandlas det till en .png.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Se även

* property [ImageType](../imagedata/imagetype/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)


