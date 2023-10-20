---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words für .NET
description: ImageSaveOptions TiffCompression eigendom. Ruft den Komprimierungstyp ab der beim Speichern generierter Bilder im TIFFFormat angewendet werden soll oder legt diesen fest in C#.
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

Hat nur Auswirkungen, wenn im TIFF-Format gespeichert wird.

Der Standardwert istLzw.

## Beispiele

Zeigt, wie Sie das Komprimierungsschema auswählen, das auf ein Dokument angewendet werden soll, das wir in ein TIFF-Bild konvertieren.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Erstellen Sie ein „ImageSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
            // um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.None“, um beim Speichern keine Komprimierung anzuwenden.
            // was zu einer sehr großen Ausgabedatei führen kann.
            // Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.Rle“, um die RLE-Komprimierung anzuwenden
            // Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.Lzw“, um die LZW-Komprimierung anzuwenden.
            // Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.Ccitt3“, um die CCITT3-Komprimierung anzuwenden.
            // Setzen Sie die Eigenschaft „TiffCompression“ auf „TiffCompression.Ccitt4“, um die CCITT4-Komprimierung anzuwenden.
            options.TiffCompression = tiffCompression;

            doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);

            switch (tiffCompression)
            {
                case TiffCompression.None:
                    Assert.That(3000000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Rle:
#if NET5_0_OR_GREATER
                    Assert.That(6000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#else
                    Assert.That(600000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#endif
                    break;
                case TiffCompression.Lzw:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt3:
                    Assert.That(90000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt4:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
            }
```

### Siehe auch

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
