---
title: CssStyleSheetType Enum
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words.CssStyleSheetType migliora l'esportazione HTML ottimizzando gli stili CSS per una migliore presentazione e prestazioni web.
type: docs
weight: 5630
url: /it/net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

Specifica come gli stili CSS (Cascading Style Sheet) vengono esportati in HTML.

```csharp
public enum CssStyleSheetType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Inline | `0` | Gli stili CSS vengono scritti in linea (come valore del**stile** attributo su ogni elemento). |
| Embedded | `1` | Gli stili CSS vengono scritti separatamente dal contenuto in un foglio di stile incorporato nel file HTML. |
| External | `2` | Gli stili CSS vengono scritti separatamente dal contenuto di un foglio di stile in un file esterno. Il file HTML collega il foglio di stile. |

## Esempi

Mostra come lavorare con i fogli di stile CSS creati da una conversione HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Creiamo un oggetto "HtmlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui convertiamo il documento in HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Imposta la proprietà "CssStylesheetType" su "CssStyleSheetType.External" per
    // accompagna un documento HTML salvato con un file di foglio di stile CSS esterno.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Di seguito sono riportati due modi per specificare directory e nomi di file per i fogli di stile CSS di output.
    // 1 - Utilizzare la proprietà "CssStyleSheetFileName" per assegnare un nome file al nostro foglio di stile:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Utilizza un callback personalizzato per nominare il nostro foglio di stile:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Imposta un nome file personalizzato, insieme ad altri parametri per un foglio di stile CSS esterno.
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
        // Possiamo accedere all'intero documento sorgente tramite la proprietà "Documento".
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

### Guarda anche

* property [CssStyleSheetType](../htmlsaveoptions/cssstylesheettype/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
