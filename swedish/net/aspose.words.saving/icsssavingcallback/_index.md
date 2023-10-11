---
title: Interface ICssSavingCallback
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.ICssSavingCallback gränssnitt. Implementera detta gränssnitt om du vill styra hur Aspose.Words sparar CSS Cascading Style Sheet när sparar ett dokument till HTML.
type: docs
weight: 5130
url: /sv/net/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface

Implementera detta gränssnitt om du vill styra hur Aspose.Words sparar CSS (Cascading Style Sheet) när sparar ett dokument till HTML.

```csharp
public interface ICssSavingCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [CssSaving](../../aspose.words.saving/icsssavingcallback/csssaving/)(CssSavingArgs) | Anropas när Aspose.Words sparar en CSS (Cascading Style Sheet). |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


