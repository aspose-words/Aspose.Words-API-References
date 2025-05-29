---
title: PageSavingArgs Class
linktitle: PageSavingArgs
articleTitle: PageSavingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.PageSavingArgs, viktig för att optimera dokumentbehandling med detaljerad PageSaving-händelsedata. Förbättra ditt arbetsflöde!
type: docs
weight: 6160
url: /sv/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

Tillhandahåller data för[`PageSaving`](../ipagesavingcallback/pagesaving/) händelse.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class PageSavingArgs
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PageSavingArgs](pagesavingargs/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en dokumentsida har sparats. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | Hämtar eller anger filnamnet där dokumentsidan ska sparas. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | Aktuell sidindex. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | Gör det möjligt att ange strömmen där dokumentsidan ska sparas. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
