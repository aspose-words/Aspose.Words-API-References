---
title: FixedPageSaveOptions.JpegQuality
second_title: Aspose.Words für .NET-API-Referenz
description: FixedPageSaveOptions eigendom. Ruft einen Wert ab oder legt diesen fest der die Qualität der JPEGBilder im HTMLDokument bestimmt.
type: docs
weight: 20
url: /de/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Ruft einen Wert ab oder legt diesen fest, der die Qualität der JPEG-Bilder im HTML-Dokument bestimmt.

```csharp
public int JpegQuality { get; set; }
```

### Bemerkungen

Hat nur Auswirkungen, wenn ein Dokument JPEG-Bilder enthält.

Verwenden Sie diese Eigenschaft, um die Qualität der Bilder in einem Dokument beim Speichern im festen Seitenformat abzurufen oder festzulegen. Der Wert kann zwischen 0 und 100 variieren, wobei 0 die schlechteste Qualität, aber maximale Komprimierung und 100 die beste Qualität, aber minimale Komprimierung bedeutet.

Der Standardwert ist 95.

### Beispiele

Zeigt, wie die Komprimierung beim Speichern eines Dokuments als JPEG konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein „ImageSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Setzen Sie die Eigenschaft „JpegQuality“ auf „10“, um beim Rendern des Dokuments eine stärkere Komprimierung zu verwenden.
// Dadurch wird die Dateigröße des Dokuments verringert, das Bild weist jedoch deutlichere Komprimierungsartefakte auf.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Setzen Sie die Eigenschaft „JpegQuality“ auf „100“, um beim Rendern des Dokuments eine schwächere Komprimierung zu verwenden.
// Dies verbessert die Qualität des Bildes auf Kosten einer größeren Dateigröße.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Siehe auch

* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* Montage [Aspose.Words](../../../)


