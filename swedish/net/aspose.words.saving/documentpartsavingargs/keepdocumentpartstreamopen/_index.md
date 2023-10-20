---
title: DocumentPartSavingArgs.KeepDocumentPartStreamOpen
linktitle: KeepDocumentPartStreamOpen
articleTitle: KeepDocumentPartStreamOpen
second_title: Aspose.Words för .NET
description: DocumentPartSavingArgs KeepDocumentPartStreamOpen fast egendom. Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att ha sparat en dokumentdel i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs.KeepDocumentPartStreamOpen property

Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att ha sparat en dokumentdel.

```csharp
public bool KeepDocumentPartStreamOpen { get; set; }
```

## Anmärkningar

Standard är`falsk` och Aspose.Words kommer att stänga strömmen du angav i[`DocumentPartStream`](../documentpartstream/) egenskap efter att ha skrivit en dokumentdel i den. Specificera`Sann` för att hålla strömmen öppen. Observera att huvudutgångsströmmen tillhandahålls i anropet till[`Save`](../../../aspose.words/document/save/)eller [`Save`](../../../aspose.words/document/save/) kommer aldrig att stängas av Aspose.Words även om`KeepDocumentPartStreamOpen` är satt till`falsk`.

## Exempel

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

* class [DocumentPartSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
