---
title: ImageSavingArgs.KeepImageStreamOpen
second_title: Aspose.Words för .NET API Referens
description: ImageSavingArgs fast egendom. Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en bild har sparats.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en bild har sparats.

```csharp
public bool KeepImageStreamOpen { get; set; }
```

### Anmärkningar

Standard är`falsk` och Aspose.Words kommer att stänga strömmen du angav i[`ImageStream`](../imagestream/) egenskap efter att ha skrivit in en bild i den. Specificera`Sann` för att hålla strömmen öppen.

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

* class [ImageSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../imagesavingargs/)
* hopsättning [Aspose.Words](../../../)


