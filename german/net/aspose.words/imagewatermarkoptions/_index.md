---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.ImageWatermarkOptions. Passen Sie Ihre Bildwasserzeichen mühelos mit vielseitigen Optionen für eine verbesserte Dokumentpräsentation an.
type: docs
weight: 3670
url: /de/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Bild angegeben werden können.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Wasserzeichen](https://docs.aspose.com/words/net/working-with-watermark/) Dokumentationsartikel.

```csharp
public class ImageWatermarkOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert ist`WAHR` . |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | Ruft den Skalierungsfaktor als Bruchteil des Bildes ab oder legt ihn fest. Der Standardwert ist 0 (auto). |

## Beispiele

Zeigt, wie aus einem Bild im lokalen Dateisystem ein Wasserzeichen erstellt wird.

```csharp
Document doc = new Document();

            // Ändern Sie das Erscheinungsbild des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt.
            // und übergeben Sie es dann beim Erstellen eines Wasserzeichens aus einer Bilddatei.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Wir haben verschiedene Möglichkeiten, Bilder einzufügen:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
