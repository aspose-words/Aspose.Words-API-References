---
title: IPageSavingCallback.PageSaving
linktitle: PageSaving
articleTitle: PageSaving
second_title: Aspose.Words för .NET
description: Upptäck iPageSavingCallback-metoden i Aspose.Words, utformad för att optimera sidsparning till fasta format. Förbättra din dokumenthantering idag!
type: docs
weight: 10
url: /sv/net/aspose.words.saving/ipagesavingcallback/pagesaving/
---
## IPageSavingCallback.PageSaving method

Anropas när Aspose.Words sparar en separat sida till fasta sidformat.

```csharp
public void PageSaving(PageSavingArgs args)
```

## Exempel

Visar hur man använder en återanropsfunktion för att spara ett dokument till HTML sida för sida.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Skapa ett "HtmlFixedSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur vi konverterar dokumentet till HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Vi sparar varje sida i det här dokumentet till en separat HTML-fil i det lokala filsystemet.
    // Ställ in en återanropsfunktion som låter oss namnge varje HTML-dokument som utdata.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Sparar alla sidor till en fil och katalog som anges i.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Nedan följer två sätt att ange var Aspose.Words ska spara varje sida i dokumentet.
        // 1 - Ange ett filnamn för utdatafilen:
        args.PageFileName = outFileName;

        // 2 - Skapa en anpassad ström för utdatafilen:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Se även

* class [PageSavingArgs](../../pagesavingargs/)
* interface [IPageSavingCallback](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
