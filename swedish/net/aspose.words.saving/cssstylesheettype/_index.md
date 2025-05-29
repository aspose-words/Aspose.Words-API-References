---
title: CssStyleSheetType Enum
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.CssStyleSheetType förbättrar HTML-export genom att optimera CSS-stilar för bättre webbpresentation och prestanda.
type: docs
weight: 5630
url: /sv/net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

Anger hur CSS-stilar (Cascading Style Sheet) exporteras till HTML.

```csharp
public enum CssStyleSheetType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Inline | `0` | CSS-stilar skrivs inline (som ett värde för**stil** attribut på varje element). |
| Embedded | `1` | CSS-stilar skrivs separat från innehållet i en stilmall som är inbäddad i HTML-filen. |
| External | `2` | CSS-stilar skrivs separat från innehållet i en stilmall i en extern fil. HTML-filen länkar stilmallen. |

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

* property [CssStyleSheetType](../htmlsaveoptions/cssstylesheettype/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
