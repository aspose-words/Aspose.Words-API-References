---
title: Enum ImageType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.ImageType opsomming. Gibt den Typ Format eines Bildes in einem Microsoft WordDokument an.
type: docs
weight: 950
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
| NoImage | `0` | Das sind keine Bilddaten. |
| Unknown | `1` | Ein unbekannter Bildtyp oder ein Bildtyp, der nicht direkt in einem Microsoft Word-Dokument gespeichert werden kann. |
| Emf | `2` | Erweiterte Windows-Metadatei. |
| Wmf | `3` | Windows-Metadatei. |
| Pict | `4` | Macintosh-BILD. Ein vorhandenes Bild wird in einem Dokument beibehalten, aber das Einfügen neuer PICT-Bilder in ein Dokument wird nicht unterstützt. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Tragbare Netzwerkgrafiken. |
| Bmp | `7` | Windows-Bitmap. |

### Beispiele

Zeigt, wie Sie einer Form ein Bild hinzufügen und seinen Typ überprüfen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // Das Bild in der URL ist ein .gif. Wenn Sie es in ein Dokument einfügen, wird es in eine .png-Datei konvertiert.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Siehe auch

* property [ImageType](../imagedata/imagetype/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


