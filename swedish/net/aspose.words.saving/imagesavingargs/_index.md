---
title: ImageSavingArgs Class
linktitle: ImageSavingArgs
articleTitle: ImageSavingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ImageSavingArgs, som förbättrar dokumentbehandlingen med anpassningsbara bildsparningsalternativ för optimal prestanda.
type: docs
weight: 5990
url: /sv/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Tillhandahåller data för[`ImageSaving`](../iimagesavingcallback/imagesaving/) händelse.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class ImageSavingArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Hämtar[`ShapeBase`](../../aspose.words.drawing/shapebase/) objekt som motsvarar formen eller gruppformen som ska sparas. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Hämtar dokumentobjektet som för närvarande sparas. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Hämtar eller anger filnamnet (utan sökväg) där bilden ska sparas. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Gör det möjligt att ange strömmen där bilden ska sparas. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | Returer`sann` om den aktuella bilden är tillgänglig för export. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en bild har sparats. |

## Anmärkningar

Som standard, när Aspose.Words sparar ett dokument till HTML, sparas varje bild i en separat fil. Aspose.Words använder dokumentets filnamn och ett unikt nummer för att generera ett unikt filnamn för varje bild som finns i dokumentet.

`ImageSavingArgs`låter dig omdefiniera hur bildfilnamn genereras eller att helt undvika att bilder sparas i filer genom att tillhandahålla dina egna strömobjekt.

För att använda din egen logik för att generera bildfilnamn, använd [`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) och[`IsImageAvailable`](./isimageavailable/) egenskaper.

För att spara bilder i strömmar istället för filer, använd[`ImageStream`](./imagestream/) egendom.

## Exempel

Visar hur man delar upp ett dokument i delar och sparar dem.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Skapa ett "HtmlFixedSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur vi konverterar dokumentet till HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Om vi sparar dokumentet normalt kommer det att finnas en HTML-utgång
    // dokument med allt innehåll i källdokumentet.
    // Ställ in egenskapen "DocumentSplitCriteria" till "DocumentSplitCriteria.SectionBreak" till
    // spara vårt dokument till flera HTML-filer: en för varje avsnitt.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Tilldela en anpassad återanropning till egenskapen "DocumentPartSavingCallback" för att ändra logiken för att spara dokumentdelen.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Om vi konverterar ett dokument som innehåller bilder till html, får vi en html-fil som länkar till flera bilder.
    // Varje bild kommer att vara i form av en fil i det lokala filsystemet.
    // Det finns också en återanropsfunktion som kan anpassa namn och filsystemplats för varje bild.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Anger anpassade filnamn för utdatadokument som sparandet delar upp ett dokument i.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Vi kan komma åt hela källdokumentet via egenskapen "Dokument".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Nedan följer två sätt att ange var Aspose.Words ska spara varje del av dokumentet.
        // 1 - Ange ett filnamn för utdatafilen:
        args.DocumentPartFileName = partFileName;

        // 2 - Skapa en anpassad ström för utdatafilen:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Anger anpassade filnamn för bildfiler som skapas vid en HTML-konvertering.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Nedan följer två sätt att ange var Aspose.Words ska spara varje del av dokumentet.
        // 1 - Ange ett filnamn för bildfilen som visas:
        args.ImageFileName = imageFileName;

        // 2 - Skapa en anpassad ström för utdatabildfilen:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
