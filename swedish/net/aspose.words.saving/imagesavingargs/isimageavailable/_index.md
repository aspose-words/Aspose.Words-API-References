---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: Aspose.Words för .NET
description: Kontrollera om en bild är redo för export med egenskapen IsImageAvailable i ImageSavingArgs. Säkerställ sömlös bildhantering och effektivitet!
type: docs
weight: 50
url: /sv/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Returer`sann` om den aktuella bilden är tillgänglig för export.

```csharp
public bool IsImageAvailable { get; }
```

## Anmärkningar

Vissa bilder i dokumentet kan vara otillgängliga, till exempel för att bilden är länkad och länken är otillgänglig eller inte pekar på en giltig bild. I det här fallet exporterar Aspose.Words en ikon med ett rött kors. Den här egenskapen returnerar `sann` om originalbilden är tillgänglig; returnerar`falsk`om den ursprungliga -bilden inte är tillgänglig och en ikon för "ingen bild" visas för sparning.

När man sparar en gruppform eller en form som inte kräver någon bild används alltid den här egenskapen `sann`.

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
