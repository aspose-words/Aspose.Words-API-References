---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words för .NET
description: Upptäck ImageStream-egenskapen i ImageSavingArgs för att enkelt ange var dina bilder ska sparas, vilket förbättrar ditt arbetsflöde och din effektivitet.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Gör det möjligt att ange strömmen där bilden ska sparas.

```csharp
public Stream ImageStream { get; set; }
```

## Anmärkningar

Den här egenskapen låter dig spara bilder till strömmar istället för filer under HTML.

Standardvärdet är`null` När den här egenskapen är`null` , kommer bilden att sparas till en fil som anges i[`ImageFileName`](../imagefilename/) egendom.

Användning[`IImageSavingCallback`](../../iimagesavingcallback/) Du kan inte ersätta en bild med en annan . Den är endast avsedd för att kontrollera var bilder ska sparas.

## Exempel

Visar hur man inkluderar en återanropsfunktion för att spara bilder i en HTML-konverteringsprocess.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt för att ange en återanropning
    // för att anpassa processen för att spara bilder.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Skriver ut egenskaperna för varje bild medan sparprocessen sparar den till en bildfil i det lokala filsystemet
/// under export av ett dokument till HTML.
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

### Se även

* class [ImageSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
