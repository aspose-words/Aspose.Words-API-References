---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageStream-Eigenschaft in ImageSavingArgs, um einfach anzugeben, wo Ihre Bilder gespeichert werden sollen, und so Ihren Arbeitsablauf und Ihre Effizienz zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Ermöglicht die Angabe des Streams, in dem das Bild gespeichert wird.

```csharp
public Stream ImageStream { get; set; }
```

## Bemerkungen

Mit dieser Eigenschaft können Sie während HTML Bilder in Streams statt in Dateien speichern.

Der Standardwert ist`null` Wenn diese Eigenschaft`null` wird das Bild in einer Datei gespeichert, die im[`ImageFileName`](../imagefilename/) Eigentum.

Verwenden[`IImageSavingCallback`](../../iimagesavingcallback/) Sie können ein Bild nicht durch ein anderes ersetzen. Es dient nur zur Kontrolle über den Speicherort der Bilder.

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
