---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.ImageWatermarkOptions. Personalizza le filigrane delle tue immagini senza sforzo con opzioni versatili per una presentazione migliore dei documenti.
type: docs
weight: 3670
url: /it/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

Contiene opzioni che possono essere specificate quando si aggiunge una filigrana con un'immagine.

Per saperne di più, visita il[Lavorare con la filigrana](https://docs.aspose.com/words/net/working-with-watermark/) articolo di documentazione.

```csharp
public class ImageWatermarkOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | Ottiene o imposta un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana. Il valore predefinito è`VERO` . |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | Ottiene o imposta il fattore di scala espresso come frazione dell'immagine. Il valore predefinito è 0 - auto. |

## Esempi

Mostra come creare una filigrana da un'immagine nel file system locale.

```csharp
Document doc = new Document();

            // Modifica l'aspetto della filigrana dell'immagine con un oggetto ImageWatermarkOptions,
            // quindi passarlo durante la creazione di una filigrana da un file immagine.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Abbiamo diverse opzioni per inserire l'immagine:
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

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
