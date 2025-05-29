---
title: HtmlSaveOptions.CssStyleSheetType
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen CssStyleSheetType i HtmlSaveOptions optimerar CSS-export till HTML-, MHTML- och EPUB-format för sömlös integration.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/htmlsaveoptions/cssstylesheettype/
---
## HtmlSaveOptions.CssStyleSheetType property

Anger hur CSS-stilar (Cascading Style Sheet) exporteras till HTML, MHTML eller EPUB. Standardvärdet ärInline för HTML/MHTML och External för EPUB.

```csharp
public CssStyleSheetType CssStyleSheetType { get; set; }
```

## Anmärkningar

Att spara CSS-stilmallar i en extern fil stöds endast när du sparar till HTML. När du exporterar till ett av containerformaten (EPUB eller MHTML) och anger External, CSS-filen kommer att inkapslas i utdatapaketet.

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

* property [CssStyleSheetFileName](../cssstylesheetfilename/)
* enum [CssStyleSheetType](../../cssstylesheettype/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
