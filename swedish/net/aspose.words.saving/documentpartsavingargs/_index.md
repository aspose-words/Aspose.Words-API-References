---
title: Class DocumentPartSavingArgs
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.DocumentPartSavingArgs klass. Tillhandahåller data förDocumentPartSaving callback.
type: docs
weight: 4680
url: /sv/net/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class

Tillhandahåller data för[`DocumentPartSaving`](../idocumentpartsavingcallback/documentpartsaving/) callback.

```csharp
public class DocumentPartSavingArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.saving/documentpartsavingargs/document/) { get; } | Hämtar dokumentobjektet som sparas. |
| [DocumentPartFileName](../../aspose.words.saving/documentpartsavingargs/documentpartfilename/) { get; set; } | Hämtar eller ställer in filnamnet (utan sökväg) där dokumentdelen ska sparas. |
| [DocumentPartStream](../../aspose.words.saving/documentpartsavingargs/documentpartstream/) { get; set; } | Tillåter att ange strömmen där dokumentdelen ska sparas. |
| [KeepDocumentPartStreamOpen](../../aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/) { get; set; } | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att ha sparat en dokumentdel. |

### Anmärkningar

När Aspose.Words sparar ett dokument till HTML eller relaterade format och[`DocumentSplitCriteria`](../htmlsaveoptions/documentsplitcriteria/) anges, dokumentet delas upp i delar och som standard sparas varje dokumentdel i en separat fil.

Klass`DocumentPartSavingArgs` låter dig styra hur varje dokumentdel ska sparas. Det gör det möjligt att omdefiniera hur filnamn genereras eller att helt kringgå lagring av dokumentdelar i -filer genom att tillhandahålla dina egna strömobjekt.

För att spara dokumentdelar i strömmar istället för filer, använd[`DocumentPartStream`](./documentpartstream/) fast egendom.

### Exempel

Visar hur man delar upp ett dokument i delar och sparar dem.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Skapa ett "HtmlFixedSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
    // för att ändra hur vi konverterar dokumentet till HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Om vi sparar dokumentet normalt kommer det att finnas en HTML-utdata
    // dokument med allt källdokumentets innehåll.
    // Ställ in egenskapen "DocumentSplitCriteria" till "DocumentSplitCriteria.SectionBreak" till
    // spara vårt dokument i flera HTML-filer: en för varje avsnitt.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Tilldela en anpassad återuppringning till egenskapen "DocumentPartSavingCallback" för att ändra logiken för att spara dokumentdelen.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Om vi konverterar ett dokument som innehåller bilder till html kommer vi att få en html-fil som länkar till flera bilder.
    // Varje bild kommer att vara i form av en fil i det lokala filsystemet.
    // Det finns också en återuppringning som kan anpassa namnet och filsystemets plats för varje bild.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Ställer in anpassade filnamn för utdatadokument som sparoperationen delar upp ett dokument i.
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

        // Nedan finns två sätt att specificera var Aspose.Words kommer att spara varje del av dokumentet.
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
/// Ställer in anpassade filnamn för bildfiler som en HTML-konvertering skapar.
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

        // Nedan finns två sätt att specificera var Aspose.Words kommer att spara varje del av dokumentet.
        // 1 - Ange ett filnamn för utdatafilen:
        args.ImageFileName = imageFileName;

        // 2 - Skapa en anpassad ström för utdatafilen:
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


