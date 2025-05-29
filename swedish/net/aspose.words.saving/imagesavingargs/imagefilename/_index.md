---
title: ImageSavingArgs.ImageFileName
linktitle: ImageFileName
articleTitle: ImageFileName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageSavingArgs ImageFileName för att enkelt hantera bildfilnamn och spara platser för effektiv bildhantering.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/imagesavingargs/imagefilename/
---
## ImageSavingArgs.ImageFileName property

Hämtar eller anger filnamnet (utan sökväg) där bilden ska sparas.

```csharp
public string ImageFileName { get; set; }
```

## Anmärkningar

Den här egenskapen låter dig omdefiniera hur bildfilnamnen genereras vid export till HTML.

När händelsen utlöses innehåller den här egenskapen filnamnet som genererades av Aspose.Words. Du kan ändra värdet på den här egenskapen för att spara bilden i en annan fil. Observera att filnamn måste vara unika.

Aspose.Words genererar automatiskt ett unikt filnamn för varje inbäddad bild vid export till HTML-format. Hur bildfilnamnet genereras beror på om du sparar dokumentet till en fil eller en dataström.

När man sparar ett dokument till en fil ser det genererade bildfilnamnet ut så här: &lt;dokumentets basfilnamn&gt;.&lt;bildnummer&gt;.&lt;filändelse&gt;.

När man sparar ett dokument i en dataström ser det genererade bildfilnamnet ut så här: Aspose.Words.&lt;dokumentguide&gt;.&lt;bildnummer&gt;.&lt;tillägg&gt;.

`ImageFileName` måste endast innehålla filnamnet utan sökvägen. Aspose.Words bestämmer sökvägen för att spara och värdet för`källa` attributet för att skriva till HTML med hjälp av dokumentets filnamn,[`ImagesFolder`](../../htmlsaveoptions/imagesfolder/) och [`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias/) egenskaper.

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

* class [ImageSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
