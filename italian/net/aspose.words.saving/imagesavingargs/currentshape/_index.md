---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words per .NET
description: Scopri la proprietà CurrentShape di ImageSavingArgs per accedere all'oggetto ShapeBase per un salvataggio efficiente di forme e gruppi di forme nei tuoi progetti.
type: docs
weight: 10
url: /it/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Ottiene il[`ShapeBase`](../../../aspose.words.drawing/shapebase/) oggetto corrispondente alla forma o alla forma del gruppo che sta per essere salvata.

```csharp
public ShapeBase CurrentShape { get; }
```

## Osservazioni

[`IImageSavingCallback`](../../iimagesavingcallback/) può essere attivato durante il salvataggio di una forma o di un gruppo di forme. Ecco perché la proprietà ha[`ShapeBase`](../../../aspose.words.drawing/shapebase/) tipo. Puoi verificare se si tratta di una forma di gruppo confrontando [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) conGroup o convertendolo in una delle classi derivate: [`Shape`](../../../aspose.words.drawing/shape/) O[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words utilizza il nome del file del documento e un numero univoco per generare il nome file univoco per ogni immagine presente nel documento. È possibile utilizzare`CurrentShape`proprietà per generare un nome di file "migliore" esaminando le proprietà della forma come[`Title`](../../../aspose.words.drawing/imagedata/title/) (solo forma),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Solo forma) e[`Name`](../../../aspose.words.drawing/shapebase/name/)Naturalmente è possibile creare nomi di file utilizzando qualsiasi altra proprietà o criterio , ma si noti che i nomi di file sussidiari devono essere univoci all'interno dell'operazione di esportazione.

Alcune immagini nel documento potrebbero non essere disponibili. Per verificare la disponibilità delle immagini utilizzare[`IsImageAvailable`](../isimageavailable/) proprietà.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
