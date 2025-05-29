---
title: DocumentPartSavingArgs Class
linktitle: DocumentPartSavingArgs
articleTitle: DocumentPartSavingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.DocumentPartSavingArgs, viktig för att förbättra dokumentbehandling med anpassningsbara sparalternativ och effektiva återanrop.
type: docs
weight: 5690
url: /sv/net/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class

Tillhandahåller data för[`DocumentPartSaving`](../idocumentpartsavingcallback/documentpartsaving/) återuppringning.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class DocumentPartSavingArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.saving/documentpartsavingargs/document/) { get; } | Hämtar dokumentobjektet som sparas. |
| [DocumentPartFileName](../../aspose.words.saving/documentpartsavingargs/documentpartfilename/) { get; set; } | Hämtar eller anger filnamnet (utan sökväg) där dokumentdelen ska sparas. |
| [DocumentPartStream](../../aspose.words.saving/documentpartsavingargs/documentpartstream/) { get; set; } | Gör det möjligt att ange strömmen där dokumentdelen ska sparas. |
| [KeepDocumentPartStreamOpen](../../aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/) { get; set; } | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en dokumentdel har sparats. |

## Anmärkningar

När Aspose.Words sparar ett dokument till HTML eller relaterade format och[`DocumentSplitCriteria`](../htmlsaveoptions/documentsplitcriteria/)Om anges delas dokumentet upp i delar och som standard sparas varje dokumentdel i en separat fil.

Klass`DocumentPartSavingArgs` låter dig kontrollera hur varje dokumentdel sparas. Det gör det möjligt att omdefiniera hur filnamn genereras eller att helt undvika att dokumentdelar sparas i filer genom att tillhandahålla dina egna strömobjekt.

För att spara dokumentdelar i strömmar istället för filer, använd[`DocumentPartStream`](./documentpartstream/) egendom.

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
