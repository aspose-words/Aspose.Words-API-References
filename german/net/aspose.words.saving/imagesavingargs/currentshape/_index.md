---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words für .NET
description: ImageSavingArgs CurrentShape eigendom. Ruft die abShapeBase Objekt das der Form oder Gruppenform entspricht die gespeichert werden soll in C#.
type: docs
weight: 10
url: /de/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Ruft die ab[`ShapeBase`](../../../aspose.words.drawing/shapebase/) Objekt, das der Form oder Gruppenform entspricht, die gespeichert werden soll.

```csharp
public ShapeBase CurrentShape { get; }
```

## Bemerkungen

[`IImageSavingCallback`](../../iimagesavingcallback/) kann beim Speichern einer Form oder einer Gruppenform ausgelöst werden. Deshalb hat die Immobilie[`ShapeBase`](../../../aspose.words.drawing/shapebase/) Typ. Sie können überprüfen, ob es sich um eine Gruppenform handelt, indem Sie vergleichen.[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) mitGroup oder durch Umwandlung in eine der abgeleiteten Klassen: [`Shape`](../../../aspose.words.drawing/shape/) oder[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words verwendet den Dateinamen des Dokuments und eine eindeutige Nummer, um für jedes im Dokument gefundene Bild einen eindeutigen Dateinamen zu generieren. Du kannst den ... benutzen`CurrentShape`Eigenschaft, um einen „besseren“ Dateinamen zu generieren, indem Formeigenschaften wie untersucht werden[`Title`](../../../aspose.words.drawing/imagedata/title/) (nur Form),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Nur Form) und[`Name`](../../../aspose.words.drawing/shapebase/name/). Natürlich können Sie Dateinamen mit beliebigen anderen Eigenschaften oder Kriterien erstellen , aber beachten Sie, dass untergeordnete Dateinamen innerhalb des Exportvorgangs eindeutig sein müssen.

Einige Bilder im Dokument sind möglicherweise nicht verfügbar. Um die Bildverfügbarkeit zu überprüfen, verwenden Sie [`IsImageAvailable`](../isimageavailable/) Eigentum.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
