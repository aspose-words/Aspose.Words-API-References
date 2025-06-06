---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: Aspose.Words per .NET
description: Controlla se un'immagine è pronta per l'esportazione con la proprietà IsImageAvailable in ImageSavingArgs. Garantisci una gestione delle immagini impeccabile ed efficiente!
type: docs
weight: 50
url: /it/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Restituisce`VERO` se l'immagine corrente è disponibile per l'esportazione.

```csharp
public bool IsImageAvailable { get; }
```

## Osservazioni

Alcune immagini nel documento potrebbero non essere disponibili, ad esempio perché l'immagine è collegata e il collegamento non è accessibile o non punta a un'immagine valida. In questo caso, Aspose.Words esporta un'icona con una croce rossa. Questa proprietà restituisce `VERO` se l'immagine originale è disponibile; restituisce`falso`se l'immagine originale non è disponibile, verrà visualizzata un'icona "nessuna immagine" per il salvataggio.

Quando si salva una forma di gruppo o una forma che non richiede alcuna immagine, questa proprietà è sempre`VERO`.

## Esempi

Mostra come coinvolgere un callback di salvataggio delle immagini in un processo di conversione HTML.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per designare un callback
    // per personalizzare il processo di salvataggio delle immagini.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Stampa le proprietà di ciascuna immagine mentre il processo di salvataggio la salva in un file immagine nel file system locale
/// durante l'esportazione di un documento in HTML.
/// </summary>
private class ImageShapePrinter : IImageSavingCallback
{
    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        args.KeepImageStreamOpen = false;
        Assert.True(args.IsImageAvailable);

        Console.WriteLine($"{args.Document.OriginalFileName.Split('\\').Last()} Image #{++mImageCount}");

        LayoutCollector layoutCollector = new LayoutCollector(args.Document);

        Console.WriteLine($"\tOn page:\t{layoutCollector.GetStartPageIndex(args.CurrentShape)}");
        Console.WriteLine($"\tDimensions:\t{args.CurrentShape.Bounds}");
        Console.WriteLine($"\tAlignment:\t{args.CurrentShape.VerticalAlignment}");
        Console.WriteLine($"\tWrap type:\t{args.CurrentShape.WrapType}");
        Console.WriteLine($"Output filename:\t{args.ImageFileName}\n");
    }

    private int mImageCount;
}
```

### Guarda anche

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
