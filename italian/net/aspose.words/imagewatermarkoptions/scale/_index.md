---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words per .NET
description: Scopri la proprietà Scala di ImageWatermarkOptions per regolare facilmente il ridimensionamento dell'immagine e ottenere una filigrana ottimale. Valore predefinito: 0 automatico per un'integrazione perfetta.
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
| ArgumentOutOfRangeException | Generato quando l'argomento non rientra nell'intervallo di valori validi. |

## Osservazioni

I valori validi vanno da 0 a 65,5 inclusi.

La scala automatica significa che la filigrana verrà ridimensionata alla sua larghezza e altezza massime rispetto ai margini della pagina.

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
