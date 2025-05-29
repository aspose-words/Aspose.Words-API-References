---
title: CssSavingArgs.CssStream
linktitle: CssStream
articleTitle: CssStream
second_title: Aspose.Words för .NET
description: Optimera din CSS-lagring med egenskapen CssSavingArgs CssStream, vilket möjliggör sömlös sparning av CSS-data till din föredragna ström.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/csssavingargs/cssstream/
---
## CssSavingArgs.CssStream property

Gör det möjligt att ange strömmen där CSS-informationen ska sparas.

```csharp
public Stream CssStream { get; set; }
```

## Anmärkningar

Den här egenskapen låter dig spara CSS-information till en ström.

Standardvärdet är`null`Den här egenskapen förhindrar inte att CSS-information sparas i en fil eller att den bäddas in i ett HTML-dokument. För att förhindra export av CSS, använd[`IsExportNeeded`](../isexportneeded/) egendom.

Användning[`ICssSavingCallback`](../../icsssavingcallback/) Du kan inte ersätta CSS med något annat. Det är endast avsett för att spara CSS i en ström.

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

* class [CssSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
