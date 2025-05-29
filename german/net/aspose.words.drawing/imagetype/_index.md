---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Drawing.ImageType zur einfachen Verwaltung von Bildformaten in Microsoft Word-Dokumenten. Verbessern Sie die visuelle Attraktivität Ihres Dokuments!
type: docs
weight: 1410
url: /de/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Gibt den Typ (das Format) eines Bildes in einem Microsoft Word-Dokument an.

```csharp
public enum ImageType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| NoImage | `0` | Es sind keine Bilddaten vorhanden. |
| Unknown | `1` | Ein unbekannter Bildtyp oder ein Bildtyp, der nicht direkt in einem Microsoft Word-Dokument gespeichert werden kann. |
| Emf | `2` | Erweiterte Windows-Metadatei. |
| Wmf | `3` | Windows-Metadatei. |
| Pict | `4` | Macintosh PICT. Ein vorhandenes Bild bleibt in einem Dokument erhalten, das Einfügen neuer PICT-Bilder in ein Dokument wird jedoch nicht unterstützt. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Tragbare Netzwerkgrafiken. |
| Bmp | `7` | Windows Bitmap. |
| Eps | `8` | Gekapseltes PostScript. |
| WebP | `9` | WebP. |
| Gif | `10` | GIF |

## Beispiele

Zeigt, wie WebP-Bilder gelesen werden.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

Zeigt, wie man einer Form ein Bild hinzufügt und seinen Typ überprüft.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### Siehe auch

* property [ImageType](../imagedata/imagetype/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
