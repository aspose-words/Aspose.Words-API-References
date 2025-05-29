---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words für .NET
description: Optimieren Sie die JPEG-Qualität Ihrer HTML-Dokumente mit FixedPageSaveOptions. Passen Sie die JpegQuality-Eigenschaft einfach an und erzielen Sie eine beeindruckende Bildschärfe.
type: docs
weight: 20
url: /de/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Ruft einen Wert ab oder legt ihn fest, der die Qualität der JPEG-Bilder im HTML-Dokument bestimmt.

```csharp
public int JpegQuality { get; set; }
```

## Bemerkungen

Hat nur Auswirkungen, wenn ein Dokument JPEG-Bilder enthält.

Verwenden Sie diese Eigenschaft, um die Qualität der Bilder in einem Dokument beim Speichern im festen Seitenformat abzurufen oder festzulegen. Der Wert kann zwischen 0 und 100 variieren, wobei 0 die schlechteste Qualität, aber maximale Komprimierung und 100 die beste Qualität, aber minimale Komprimierung bedeutet.

Der Standardwert ist 95.

## Beispiele

Zeigt, wie die Komprimierung beim Speichern eines Dokuments als JPEG konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild umwandelt.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Setzen Sie die Eigenschaft „JpegQuality“ auf „10“, um beim Rendern des Dokuments eine stärkere Komprimierung zu verwenden.
// Dadurch wird die Dateigröße des Dokuments reduziert, das Bild weist jedoch deutlichere Komprimierungsartefakte auf.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Setzen Sie die Eigenschaft „JpegQuality“ auf „100“, um beim Rendern des Dokuments eine schwächere Komprimierung zu verwenden.
// Dadurch wird die Bildqualität verbessert, allerdings erhöht sich die Dateigröße.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### Siehe auch

* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
