---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsWashout di ImageWatermarkOptions. Controlla facilmente l'effetto di sbiadimento della tua filigrana con questa semplice impostazione booleana.
type: docs
weight: 20
url: /it/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Ottiene o imposta un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana. Il valore predefinito è`VERO` .

```csharp
public bool IsWashout { get; set; }
```

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

* class [ImageWatermarkOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
