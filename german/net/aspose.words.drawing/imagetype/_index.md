---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.ImageType opsomming. Gibt den Typ Format eines Bildes in einem Microsoft WordDokument an in C#.
type: docs
weight: 1080
url: /de/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Gibt den Typ (Format) eines Bildes in einem Microsoft Word-Dokument an.

```csharp
public enum ImageType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| NoImage | `0` | Es liegen keine Bilddaten vor. |
| Unknown | `1` | Ein unbekannter Bildtyp oder Bildtyp, der nicht direkt in einem Microsoft Word-Dokument gespeichert werden kann. |
| Emf | `2` | Windows Enhanced Metafile. |
| Wmf | `3` | Windows-Metadatei. |
| Pict | `4` | Macintosh BILD. Ein vorhandenes Bild bleibt in einem Dokument erhalten, das Einfügen neuer PICT-Bilder in ein Dokument wird jedoch nicht unterstützt. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Tragbare Netzwerkgrafiken. |
| Bmp | `7` | Windows-Bitmap. |
| Eps | `8` | Encapsulated PostScript. |

## Beispiele

Zeigt, wie man einer Form ein Bild hinzufügt und seinen Typ überprüft.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // Das Bild in der URL ist ein .gif. Wenn Sie es in ein Dokument einfügen, wird es in eine PNG-Datei konvertiert.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Siehe auch

* property [ImageType](../imagedata/imagetype/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
