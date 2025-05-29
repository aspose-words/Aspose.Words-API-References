---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.TiffCompression für optimales Speichern von TIFF-Dateien. Wählen Sie mühelos den besten Komprimierungstyp für hochwertige Seitenbilder.
type: docs
weight: 6430
url: /de/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Gibt an, welche Art von Komprimierung beim Speichern von Seitenbildern in einer TIFF-Datei angewendet werden soll.

```csharp
public enum TiffCompression
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Gibt keine Komprimierung an. |
| Rle | `1` | Gibt das RLE-Komprimierungsschema an. |
| Lzw | `2` | Gibt das LZW-Komprimierungsschema an. In Java durch Deflate (Zip)-Komprimierung emuliert. |
| Ccitt3 | `3` | Gibt das CCITT3-Komprimierungsschema an. |
| Ccitt4 | `4` | Gibt das CCITT4-Komprimierungsschema an. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
