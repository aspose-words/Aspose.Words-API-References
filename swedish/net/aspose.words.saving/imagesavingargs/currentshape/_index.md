---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageSavingArgs CurrentShape för att komma åt ShapeBase-objektet för effektiv sparning av former och grupper av former i dina projekt.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Hämtar[`ShapeBase`](../../../aspose.words.drawing/shapebase/) objekt som motsvarar formen eller gruppformen som ska sparas.

```csharp
public ShapeBase CurrentShape { get; }
```

## Anmärkningar

[`IImageSavingCallback`](../../iimagesavingcallback/) kan utlösas medan antingen en form eller en gruppform sparas. Det är därför egenskapen har[`ShapeBase`](../../../aspose.words.drawing/shapebase/) typ. Du kan kontrollera om det är en gruppform som jämför [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) medGroup eller genom att casta den till en av de härledda klasserna: [`Shape`](../../../aspose.words.drawing/shape/) eller[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words använder dokumentets filnamn och ett unikt nummer för att generera ett unikt filnamn för varje bild som finns i dokumentet. Du kan använda`CurrentShape`egenskap för att generera ett "bättre" filnamn genom att undersöka formegenskaper som[`Title`](../../../aspose.words.drawing/imagedata/title/) (Endast form),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Endast form) och[`Name`](../../../aspose.words.drawing/shapebase/name/)Naturligtvis kan du skapa filnamn med hjälp av andra egenskaper eller kriterier men observera att underordnade filnamn måste vara unika inom exportåtgärden.

Vissa bilder i dokumentet kan vara otillgängliga. För att kontrollera bildtillgängligheten , använd[`IsImageAvailable`](../isimageavailable/) egendom.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
