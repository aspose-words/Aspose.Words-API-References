---
title: ImageSaveOptions.JpegQuality
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSaveOptions eigendom. Ruft einen Wert ab oder legt einen Wert fest der die Qualität der generierten JPEGBilder bestimmt.
type: docs
weight: 70
url: /de/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

Ruft einen Wert ab oder legt einen Wert fest, der die Qualität der generierten JPEG-Bilder bestimmt.

```csharp
public int JpegQuality { get; set; }
```

### Bemerkungen

Hat nur Auswirkung beim Speichern im JPEG-Format.

Verwenden Sie diese Eigenschaft, um die Qualität der generierten Bilder beim Speichern im JPEG-Format abzurufen oder festzulegen. Der Wert kann zwischen 0 und 100 variieren, wobei 0 die schlechteste Qualität, aber maximale Komprimierung und 100 die beste Qualität, aber minimale Komprimierung bedeutet.

Der Standardwert ist 95.

### Beispiele

Zeigt, wie die Komprimierung konfiguriert wird, während ein Dokument als JPEG gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, in der diese Methode das Dokument in ein Bild rendert.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Setzen Sie die Eigenschaft "JpegQuality" auf "10", um beim Rendern des Dokuments eine stärkere Komprimierung zu verwenden.
// Dadurch wird die Dateigröße des Dokuments reduziert, aber das Bild zeigt deutlichere Komprimierungsartefakte.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Legen Sie die Eigenschaft "JpegQuality" auf "100" fest, um beim Rendern des Dokuments eine schwächere Komprimierung zu verwenden.
// Dadurch wird die Bildqualität auf Kosten einer erhöhten Dateigröße verbessert.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions/)
* Montage [Aspose.Words](../../../)


