---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: Aspose.Words für .NET
description: Überprüfen Sie mit der Eigenschaft IsImageAvailable in ImageSavingArgs, ob ein Bild zum Export bereit ist. Sorgen Sie für reibungsloses Bildmanagement und Effizienz!
type: docs
weight: 50
url: /de/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Rückgaben`WAHR` ob das aktuelle Bild zum Export verfügbar ist.

```csharp
public bool IsImageAvailable { get; }
```

## Bemerkungen

Einige Bilder im Dokument sind möglicherweise nicht verfügbar, beispielsweise weil das Bild verknüpft ist und der Link nicht zugänglich ist oder nicht auf ein gültiges Bild verweist. In diesem Fall exportiert Aspose.Words ein Symbol mit einem roten Kreuz. Diese Eigenschaft gibt zurück.`WAHR` wenn das Originalbild verfügbar ist; gibt zurück`FALSCH`wenn das ursprüngliche -Bild nicht verfügbar ist, wird zum Speichern ein Symbol „Kein Bild“ angeboten.

Beim Speichern einer Gruppenform oder einer Form, die kein Bild benötigt, ist diese Eigenschaft immer`WAHR`.

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
