---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words für .NET
description: ImageWatermarkOptions IsWashout eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert istWAHR  in C#.
type: docs
weight: 20
url: /de/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Ruft einen booleschen Wert ab oder legt diesen fest, der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert ist`WAHR` .

```csharp
public bool IsWashout { get; set; }
```

## Beispiele

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
