---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsWashout-Eigenschaft von ImageWatermarkOptions. Steuern Sie den Auswascheffekt Ihres Wasserzeichens mühelos mit dieser einfachen booleschen Einstellung.
type: docs
weight: 20
url: /de/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Ruft einen booleschen Wert ab oder legt ihn fest, der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert ist`WAHR` .

```csharp
public bool IsWashout { get; set; }
```

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
