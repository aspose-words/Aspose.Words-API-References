---
title: CssSavingArgs Class
linktitle: CssSavingArgs
articleTitle: CssSavingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.CssSavingArgs, utformad för att förbättra din dokumentbehandling med anpassningsbara CssSaving-händelsedata för optimala resultat.
type: docs
weight: 5620
url: /sv/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Tillhandahåller data för[`CssSaving`](../icsssavingcallback/csssaving/) händelse.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class CssSavingArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | Gör det möjligt att ange strömmen där CSS-informationen ska sparas. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Hämtar dokumentobjektet som för närvarande sparas. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | Gör det möjligt att ange om CSS-koden ska exporteras till en fil och bäddas in i ett HTML-dokument. Standardinställningen är`sann` . När den här egenskapen är`falsk` , CSS-informationen kommer inte att sparas i en CSS-fil och kommer inte att bäddas in i HTML-dokumentet. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att CSS-information har sparats. |

## Anmärkningar

Som standard, när Aspose.Words sparar ett dokument till HTML, sparas CSS-information inline (som ett värde för**stil** attribut på varje element).

`CssSavingArgs` låter dig spara CSS-information i en fil genom att tillhandahålla ditt eget stream-objekt.

För att spara CSS i strömmen, använd[`CssStream`](./cssstream/) egendom.

För att undertrycka sparande av CSS i en fil och inbäddning i HTML-dokument, använd[`IsExportNeeded`](./isexportneeded/) egendom.

## Exempel

Visar hur man arbetar med CSS-stilmallar som skapas av en HTML-konvertering.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Skapa ett "HtmlFixedSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur vi konverterar dokumentet till HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Ställ in egenskapen "CssStylesheetType" till "CssStyleSheetType.External" för att
    // komplettera ett sparat HTML-dokument med en extern CSS-stilarksfil.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Nedan följer två sätt att ange kataloger och filnamn för CSS-formatmallar som utdata.
    // 1 - Använd egenskapen "CssStyleSheetFileName" för att tilldela ett filnamn till vårt stilark:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Använd en anpassad återuppringning för att namnge vårt stilark:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Anger ett anpassat filnamn, tillsammans med andra parametrar för ett externt CSS-stilark.
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        // Vi kan komma åt hela källdokumentet via egenskapen "Dokument".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
