---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words für .NET
description: Passen Sie die JpegQuality-Eigenschaft in ImageSaveOptions an, um die JPEG-Bildqualität für beeindruckende Grafiken und verbesserte Leistung zu optimieren. Perfekt für Entwickler!
type: docs
weight: 80
url: /de/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

Ruft einen Wert ab oder legt ihn fest, der die Qualität der generierten JPEG-Bilder bestimmt.

```csharp
public int JpegQuality { get; set; }
```

## Bemerkungen

Hat nur beim Speichern im JPEG-Format eine Wirkung.

Verwenden Sie diese Eigenschaft, um die Qualität der generierten Bilder beim Speichern im JPEG-Format abzurufen oder festzulegen. Der Wert kann zwischen 0 und 100 variieren, wobei 0 die schlechteste Qualität, aber maximale Komprimierung und 100 die beste Qualität, aber minimale Komprimierung bedeutet.

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

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
