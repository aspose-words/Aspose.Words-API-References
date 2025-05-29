---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions CssStyleSheetFileName anpassar dina HTML-exporter med en specificerad CSS-filsökväg, vilket förbättrar dokumentets stil.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

Anger sökvägen och namnet på CSS-filen (Cascading Style Sheet) som skrivs när ett dokument exporteras till HTML. Standardvärdet är en tom sträng.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## Anmärkningar

Den här egenskapen har endast effekt när ett dokument sparas i HTML-formatet och externt CSS-formatmall begärs med[`CssStyleSheetType`](../cssstylesheettype/).

Om den här egenskapen är tom sparas CSS-filen i samma mapp och med samma namn som HTML -dokumentet, men med filändelsen ".css".

Om endast sökväg men inget filnamn anges i den här egenskapen, sparas CSS-filen i den angivna mappen och har samma namn som HTML-dokumentet men med filändelsen ".css".

Om mappen som anges av den här egenskapen inte finns, skapas den automatiskt innan CSS-filen sparas.

Ett annat sätt att ange en mapp där externa CSS-filer sparas är att använda[`ResourceFolder`](../resourcefolder/) .

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

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
