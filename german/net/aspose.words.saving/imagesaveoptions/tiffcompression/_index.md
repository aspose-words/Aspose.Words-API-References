---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre TIFF-Bilder mit der TiffCompression-Eigenschaft von ImageSaveOptions, sodass Sie die beste Komprimierungsmethode für qualitativ hochwertige Ergebnisse auswählen können.
type: docs
weight: 180
url: /de/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Ruft den Komprimierungstyp ab, der beim Speichern generierter Bilder im TIFF-Format angewendet werden soll, oder legt diesen fest.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Bemerkungen

Hat nur beim Speichern im TIFF-Format eine Auswirkung.

Der Standardwert istLzw.

## Beispiele

Zeigt, wie das Komprimierungsschema ausgewählt wird, das auf ein Dokument angewendet werden soll, das wir in ein TIFF-Bild konvertieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild umwandelt.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.None“, um beim Speichern keine Komprimierung anzuwenden.
// was zu einer sehr großen Ausgabedatei führen kann.
// Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.Rle“, um die RLE-Komprimierung anzuwenden
// Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.Lzw“, um die LZW-Komprimierung anzuwenden.
// Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.Ccitt3“, um die CCITT3-Komprimierung anzuwenden.
// Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.Ccitt4“, um die CCITT4-Komprimierung anzuwenden.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### Siehe auch

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
