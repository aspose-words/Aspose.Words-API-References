---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImageStream in ImageSavingArgs per specificare facilmente dove salvare le tue immagini, migliorando il flusso di lavoro e l'efficienza.
type: docs
weight: 40
url: /it/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Consente di specificare il flusso in cui verrà salvata l'immagine.

```csharp
public Stream ImageStream { get; set; }
```

## Osservazioni

Questa proprietà consente di salvare le immagini in flussi anziché in file durante l'HTML.

Il valore predefinito è`null` Quando questa proprietà è`null` , l'immagine verrà salvata in un file specificato nel[`ImageFileName`](../imagefilename/) proprietà.

Utilizzo[`IImageSavingCallback`](../../iimagesavingcallback/) Non è possibile sostituire un'immagine con un'altra. Serve solo per controllare la posizione in cui salvare le immagini.

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

* class [ImageSavingArgs](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
