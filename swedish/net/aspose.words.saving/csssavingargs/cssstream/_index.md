---
title: CssSavingArgs.CssStream
second_title: Aspose.Words för .NET API Referens
description: CssSavingArgs fast egendom. Tillåter att ange strömmen där CSSinformationen ska sparas.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/csssavingargs/cssstream/
---
## CssSavingArgs.CssStream property

Tillåter att ange strömmen där CSS-informationen ska sparas.

```csharp
public Stream CssStream { get; set; }
```

### Anmärkningar

Den här egenskapen låter dig spara CSS-information i en stream.

Standardvärdet är`null` . Den här egenskapen förhindrar inte att CSS-information sparas till en fil eller inbäddning i HTML-dokument. För att undertrycka exporterande CSS använd[`IsExportNeeded`](../isexportneeded/) fast egendom.

Använder sig av[`ICssSavingCallback`](../../icsssavingcallback/) du kan inte ersätta CSS med med en annan. Den är endast avsedd för att spara CSS till en stream.

### Exempel

Visar hur man arbetar med CSS-formatmallar som en HTML-konvertering skapar.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Skapa ett "HtmlFixedSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
    // för att ändra hur vi konverterar dokumentet till HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Ställ in egenskapen "CssStylesheetType" till "CssStyleSheetType.External" till
    // åtfölja ett sparat HTML-dokument med en extern CSS-formatmallsfil.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Nedan finns två sätt att ange kataloger och filnamn för CSS-formatmallar.
    // 1 - Använd egenskapen "CssStyleSheetFileName" för att tilldela ett filnamn till vår stilmall:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Använd en anpassad återuppringning för att namnge vår stilmall:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Ställer in ett anpassat filnamn, tillsammans med andra parametrar för en extern CSS-stilmall.
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
* namnutrymme [Aspose.Words.Saving](../../csssavingargs/)
* hopsättning [Aspose.Words](../../../)


