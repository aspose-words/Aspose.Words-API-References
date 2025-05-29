---
title: ImageSaveOptions
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den ImageSaveOptions-Konstruktor zum Speichern von Bildern in verschiedenen Formaten wie TIFF, PNG, BMP, JPEG, EMF, EPS, WebP und SVG. Optimieren Sie Ihre Bildverwaltung!
type: docs
weight: 10
url: /de/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern gerenderter Bilder im verwendet werden kann.Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps , WebP oderSvg format.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | SaveFormat | Kann sein Tiff ,Png ,Bmp , Jpeg ,Emf ,EpsWebP oderSvg format. |

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
