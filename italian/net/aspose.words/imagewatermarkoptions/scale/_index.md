---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words per .NET
description: ImageWatermarkOptions Scale proprietà. Ottiene o imposta il fattore di scala espresso come frazione dellimmagine. Il valore predefinito è 0  auto in C#.
type: docs
weight: 30
url: /it/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Ottiene o imposta il fattore di scala espresso come frazione dell'immagine. Il valore predefinito è 0 - auto.

```csharp
public double Scale { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Viene generato quando l'argomento non rientra nell'intervallo di valori validi. |

## Osservazioni

I valori validi vanno da 0 a 65,5 inclusi.

La scala automatica significa che la filigrana verrà ridimensionata alla larghezza massima e all'altezza massima rispetto a i margini della pagina.

## Esempi

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
