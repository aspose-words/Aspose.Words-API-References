---
title: ImageWatermarkOptions.IsWashout
second_title: Aspose.Words per .NET API Reference
description: ImageWatermarkOptions proprietà. Ottiene o imposta un valore booleano responsabile delleffetto sbiadito della filigrana. Il valore predefinito èVERO .
type: docs
weight: 20
url: /it/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Ottiene o imposta un valore booleano responsabile dell'effetto sbiadito della filigrana. Il valore predefinito è`VERO` .

```csharp
public bool IsWashout { get; set; }
```

### Esempi

Mostra come creare una filigrana da un'immagine nel file system locale.

```csharp
Document doc = new Document();

            // Modifica l'aspetto della filigrana dell'immagine con un oggetto ImageWatermarkOptions,
            // quindi lo passa durante la creazione di una filigrana da un file immagine.
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

### Guarda anche

* class [ImageWatermarkOptions](../)
* spazio dei nomi [Aspose.Words](../../imagewatermarkoptions/)
* assemblea [Aspose.Words](../../../)


