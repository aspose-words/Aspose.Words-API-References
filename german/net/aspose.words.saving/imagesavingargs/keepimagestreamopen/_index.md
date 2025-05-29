---
title: ImageSavingArgs.KeepImageStreamOpen
linktitle: KeepImageStreamOpen
articleTitle: KeepImageStreamOpen
second_title: Aspose.Words für .NET
description: Entdecken Sie die KeepImageStreamOpen-Eigenschaft in ImageSavingArgs für Aspose.Words. Steuern Sie das Stream-Verhalten für effizientes Speichern von Bildern und verbesserte Leistung.
type: docs
weight: 60
url: /de/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

Gibt an, ob Aspose.Words den Stream nach dem Speichern eines Bildes geöffnet halten oder schließen soll.

```csharp
public bool KeepImageStreamOpen { get; set; }
```

## Bemerkungen

Standard ist`FALSCH` und Aspose.Words schließt den von Ihnen bereitgestellten Stream im[`ImageStream`](../imagestream/) Eigenschaft, nachdem ein Bild hineingeschrieben wurde. Geben Sie`WAHR` um den Stream offen zu halten.

## Beispiele

Zeigt, wie ein Rückruf zum Speichern von Bildern in einen HTML-Konvertierungsprozess einbezogen wird.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt übergeben, um einen Rückruf festzulegen
    // um den Bildspeichervorgang anzupassen.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Druckt die Eigenschaften jedes Bildes, während der Speichervorgang es in einer Bilddatei im lokalen Dateisystem speichert
/// beim Exportieren eines Dokuments nach HTML.
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

### Siehe auch

* class [ImageSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
