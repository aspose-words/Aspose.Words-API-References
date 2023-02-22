---
title: ImageWatermarkOptions.IsWashout
second_title: Aspose.Words für .NET-API-Referenz
description: ImageWatermarkOptions eigendom. Erhält oder setzt einen booleschen Wert der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert ist True.
type: docs
weight: 20
url: /de/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Erhält oder setzt einen booleschen Wert, der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert ist True.

```csharp
public bool IsWashout { get; set; }
```

### Beispiele

Zeigt, wie ein Wasserzeichen aus einem Bild im lokalen Dateisystem erstellt wird.

```csharp
Document doc = new Document();

            // Ändere das Aussehen des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt,
            // Übergeben Sie es dann, während Sie ein Wasserzeichen aus einer Bilddatei erstellen.
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


