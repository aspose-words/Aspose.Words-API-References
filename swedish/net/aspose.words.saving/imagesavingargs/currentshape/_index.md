---
title: ImageSavingArgs.CurrentShape
second_title: Aspose.Words för .NET API Referens
description: ImageSavingArgs fast egendom. FårShapeBase objekt som motsvarar formen eller gruppformen som håller på att sparas.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Får[`ShapeBase`](../../../aspose.words.drawing/shapebase/) objekt som motsvarar formen eller gruppformen som håller på att sparas.

```csharp
public ShapeBase CurrentShape { get; }
```

### Anmärkningar

[`IImageSavingCallback`](../../iimagesavingcallback/) kan avfyras samtidigt som du sparar antingen en form eller en gruppform. Det är därför fastigheten har[`ShapeBase`](../../../aspose.words.drawing/shapebase/) typ. Du kan kontrollera om det är en gruppform som jämför [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) medGroup eller genom att casta den till en av härledda klasser: [`Shape`](../../../aspose.words.drawing/shape/) eller[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words använder dokumentets filnamn och ett unikt nummer för att generera ett unikt filnamn för varje bild som finns i dokumentet. Du kan använda`CurrentShape`egenskap för att generera ett "bättre" filnamn genom att undersöka formegenskaper som t.ex[`Title`](../../../aspose.words.drawing/imagedata/title/) (endast form),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (endast form) och[`Name`](../../../aspose.words.drawing/shapebase/name/). Naturligtvis kan du bygga filnamn med andra egenskaper eller kriterier men observera att filnamnen måste vara unika i exportoperationen.

Vissa bilder i dokumentet kan vara otillgängliga. För att kontrollera bildtillgänglighet använd[`IsImageAvailable`](../isimageavailable/) fast egendom.

### Exempel

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../imagesavingargs/)
* hopsättning [Aspose.Words](../../../)


