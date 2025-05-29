---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImageSize di ImageSaveOptions per gestire e personalizzare facilmente le dimensioni delle immagini in pixel per risultati ottimali.
type: docs
weight: 70
url: /it/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Ottiene o imposta la dimensione di un'immagine generata in pixel.

```csharp
public Size ImageSize { get; set; }
```

## Osservazioni

Questa proprietà ha effetto solo quando si salva in formati di immagini raster.

Il valore predefinito è (0 x 0), il che significa che la dimensione dell'immagine generata verrà calcolata in base alla dimensione dell'immagine in punti, alla risoluzione e alla scala specificate.

## Esempi

Mostra come convertire ogni pagina di un documento in un'immagine TIFF separata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Creiamo un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo trasforma il documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Imposta la proprietà "PageSet" sul numero della prima pagina da
    // da cui iniziare il rendering del documento.
    options.PageSet = new PageSet(i);
    // Esporta la pagina a 2325x5325 pixel e 600 dpi.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
