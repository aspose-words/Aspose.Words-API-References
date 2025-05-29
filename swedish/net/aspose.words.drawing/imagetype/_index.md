---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.ImageType-enum för att enkelt hantera bildformat i Microsoft Word-dokument. Förbättra ditt dokuments visuella attraktionskraft!
type: docs
weight: 1410
url: /sv/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Anger typen (formatet) för en bild i ett Microsoft Word-dokument.

```csharp
public enum ImageType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| NoImage | `0` | Det finns inga bilddata. |
| Unknown | `1` | En okänd bildtyp eller bildtyp som inte kan lagras direkt i ett Microsoft Word-dokument. |
| Emf | `2` | Förbättrad Windows-metafil. |
| Wmf | `3` | Windows-metafile. |
| Pict | `4` | Macintosh PICT. En befintlig bild kommer att bevaras i ett dokument, men det stöds inte att infoga nya PICT-bilder i ett dokument. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Bärbar nätverksgrafik. |
| Bmp | `7` | Windows-bitmapp. |
| Eps | `8` | Inkapslad PostScript. |
| WebP | `9` | Webbplats. |
| Gif | `10` | GIF |

## Exempel

Visar hur man läser WebP-bilder.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

Visar hur man lägger till en bild i en form och kontrollerar dess typ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### Se även

* property [ImageType](../imagedata/imagetype/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
