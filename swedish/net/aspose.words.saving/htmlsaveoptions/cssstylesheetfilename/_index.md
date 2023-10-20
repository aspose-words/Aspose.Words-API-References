---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: Aspose.Words för .NET
description: HtmlSaveOptions CssStyleSheetFileName fast egendom. Anger sökvägen och namnet på CSSfilen Cascading Style Sheet som skrivs när ett document exporteras till HTML. Standard är en tom sträng i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

Anger sökvägen och namnet på CSS-filen (Cascading Style Sheet) som skrivs när ett document exporteras till HTML. Standard är en tom sträng.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## Anmärkningar

Den här egenskapen har endast effekt när du vill spara ett dokument i HTML-format och extern CSS-stilmall begärs med[`CssStyleSheetType`](../cssstylesheettype/).

Om den här egenskapen är tom kommer CSS-filen att sparas i samma mapp och med samma namn som HTML -dokumentet men med tillägget ".css".

Om endast sökväg men inget filnamn anges i den här egenskapen, sparas CSS-filen i mappen specific och kommer att ha samma namn som HTML-dokumentet men med tillägget ".css".

Om mappen som anges av den här egenskapen inte finns skapas den automatiskt innan CSS-filen sparas.

Ett annat sätt att ange en mapp där extern CSS-fil sparas är att använda[`ResourceFolder`](../resourcefolder/) .

## Exempel

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

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
