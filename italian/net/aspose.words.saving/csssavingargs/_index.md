---
title: CssSavingArgs Class
linktitle: CssSavingArgs
articleTitle: CssSavingArgs
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.CssSavingArgs classe. Fornisce i dati per ilCssSaving evento in C#.
type: docs
weight: 4880
url: /it/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Fornisce i dati per il[`CssSaving`](../icsssavingcallback/csssaving/) evento.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class CssSavingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | Permette di specificare il flusso in cui verranno salvate le informazioni CSS. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Ottiene l'oggetto documento attualmente in fase di salvataggio. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | Permette di specificare se il CSS verrà esportato in un file e incorporato nel documento HTML. L'impostazione predefinita è`VERO` . Quando questa proprietà è`falso` , le informazioni CSS non verranno salvate in un file CSS e non saranno incorporate nel documento HTML. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Specifica se Aspose.Words deve mantenere aperto il flusso o chiuderlo dopo aver salvato un'informazione CSS. |

## Osservazioni

Per impostazione predefinita, quando Aspose.Words salva un documento in HTML, salva le informazioni CSS inline (come valore del**stile** attributo su ogni elemento).

`CssSavingArgs`consente di salvare le informazioni CSS in un file fornendo il proprio oggetto stream.

Per salvare CSS nello stream, utilizzare il file[`CssStream`](./cssstream/) proprietà.

Per sopprimere il salvataggio dei CSS in un file e l'incorporamento nel documento HTML, utilizzare il file[`IsExportNeeded`](./isexportneeded/) proprietà.

## Esempi

Mostra come lavorare con i fogli di stile CSS creati da una conversione HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Crea un oggetto "HtmlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui convertiamo il documento in HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Imposta la proprietà "CssStylesheetType" su "CssStyleSheetType.External" su
    // accompagna un documento HTML salvato con un file di foglio di stile CSS esterno.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Di seguito sono riportati due modi per specificare directory e nomi di file per i fogli di stile CSS di output.
    // 1 - Utilizza la proprietà "CssStyleSheetFileName" per assegnare un nome file al nostro foglio di stile:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Usa un callback personalizzato per nominare il nostro foglio di stile:
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
        // Possiamo accedere all'intero documento sorgente tramite la proprietà "Document".
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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
