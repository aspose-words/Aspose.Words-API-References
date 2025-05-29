---
title: ImageSavingArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageSavingArgs-dokument för att komma åt det dokument som sparas, vilket förbättrar effektiviteten i ditt arbetsflöde och sparar tid.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/imagesavingargs/document/
---
## ImageSavingArgs.Document property

Hämtar dokumentobjektet som för närvarande sparas.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [ImageSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
