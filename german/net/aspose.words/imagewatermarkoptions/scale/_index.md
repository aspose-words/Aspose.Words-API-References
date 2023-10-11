---
title: ImageWatermarkOptions.Scale
second_title: Aspose.Words für .NET-API-Referenz
description: ImageWatermarkOptions eigendom. Ruft den als Bruchteil des Bildes ausgedrückten Skalierungsfaktor ab oder legt diesen fest. Der Standardwert ist 0  auto.
type: docs
weight: 30
url: /de/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Ruft den als Bruchteil des Bildes ausgedrückten Skalierungsfaktor ab oder legt diesen fest. Der Standardwert ist 0 - auto.

```csharp
public double Scale { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des gültigen Wertebereichs lag. |

### Bemerkungen

Gültige Werte liegen zwischen 0 und 65,5.

Automatische Skalierung bedeutet, dass das Wasserzeichen auf seine maximale Breite und maximale Höhe relativ zu den Seitenrändern skaliert wird.

### Beispiele

Zeigt, wie man aus einem Bild im lokalen Dateisystem ein Wasserzeichen erstellt.

```csharp
Document doc = new Document();

            // Ändern Sie das Erscheinungsbild des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt.
            // Übergebe es dann beim Erstellen eines Wasserzeichens aus einer Bilddatei.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Siehe auch

* class [ImageWatermarkOptions](../)
* namensraum [Aspose.Words](../../imagewatermarkoptions/)
* Montage [Aspose.Words](../../../)


