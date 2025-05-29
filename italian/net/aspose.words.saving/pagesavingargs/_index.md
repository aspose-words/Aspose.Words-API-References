---
title: PageSavingArgs Class
linktitle: PageSavingArgs
articleTitle: PageSavingArgs
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.PageSavingArgs, essenziale per ottimizzare l'elaborazione dei documenti con dati dettagliati sugli eventi PageSaving. Migliora il tuo flusso di lavoro!
type: docs
weight: 6160
url: /it/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

Fornisce dati per il[`PageSaving`](../ipagesavingcallback/pagesaving/) evento.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public class PageSavingArgs
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PageSavingArgs](pagesavingargs/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | Specifica se Aspose.Words deve mantenere aperto il flusso o chiuderlo dopo aver salvato una pagina del documento. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | Ottiene o imposta il nome del file in cui verrà salvata la pagina del documento. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | Indice della pagina corrente. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | Consente di specificare il flusso in cui verrà salvata la pagina del documento. |

## Esempi

Mostra come utilizzare un callback per salvare un documento in formato HTML pagina per pagina.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Creiamo un oggetto "HtmlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui convertiamo il documento in HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Salveremo ogni pagina di questo documento in un file HTML separato nel file system locale.
    // Imposta un callback che ci consente di nominare ciascun documento HTML di output.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Salva tutte le pagine in un file e in una directory specificati al suo interno.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Di seguito sono riportati due modi per specificare dove Aspose.Words salverà ogni pagina del documento.
        // 1 - Imposta un nome file per il file di pagina di output:
        args.PageFileName = outFileName;

        // 2 - Crea un flusso personalizzato per il file di pagina di output:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
