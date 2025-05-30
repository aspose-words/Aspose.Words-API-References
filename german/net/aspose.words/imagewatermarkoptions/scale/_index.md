---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words für .NET
description: Entdecken Sie die Skalierungseigenschaft von ImageWatermarkOptions, um die Bildskalierung für optimale Wasserzeichen einfach anzupassen. Standardwert 0 (automatisch) für nahtlose Integration.
type: docs
weight: 30
url: /de/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Ruft den Skalierungsfaktor als Bruchteil des Bildes ab oder legt ihn fest. Der Standardwert ist 0 (auto).

```csharp
public double Scale { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des Bereichs gültiger Werte liegt. |

## Bemerkungen

Gültige Werte liegen im Bereich von 0 bis einschließlich 65,5.

Automatische Skalierung bedeutet, dass das Wasserzeichen auf seine maximale Breite und Höhe relativ zu den Seitenrändern skaliert wird.

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

* class [ImageWatermarkOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
