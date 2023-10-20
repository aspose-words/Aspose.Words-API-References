---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words för .NET
description: ImageSavingArgs ImageStream fast egendom. Tillåter att ange strömmen där bilden ska sparas i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Tillåter att ange strömmen där bilden ska sparas.

```csharp
public Stream ImageStream { get; set; }
```

## Anmärkningar

Den här egenskapen låter dig spara bilder i strömmar istället för filer under HTML.

Standardvärdet är`null` . När denna fastighet är`null` , kommer bilden att sparas i en fil som anges i[`ImageFileName`](../imagefilename/) fast egendom.

Använder sig av[`IImageSavingCallback`](../../iimagesavingcallback/) du kan inte ersätta en bild med en annan. Den är endast avsedd för kontroll över var bilderna ska sparas.

## Exempel

Visar hur man involverar en bildsparande återuppringning i en HTML-konverteringsprocess.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt för att ange en återuppringning
    // för att anpassa processen för att spara bilder.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Skriver ut egenskaperna för varje bild när sparprocessen sparar den i en bildfil i det lokala filsystemet
/// under exporten av ett dokument till HTML.
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
