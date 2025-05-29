---
title: IPageSavingCallback.PageSaving
linktitle: PageSaving
articleTitle: PageSaving
second_title: Aspose.Words per .NET
description: Scopri il metodo iPageSavingCallback in Aspose.Words, progettato per ottimizzare il salvataggio delle pagine in formati fissi. Migliora la tua gestione dei documenti oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.saving/ipagesavingcallback/pagesaving/
---
## IPageSavingCallback.PageSaving method

Chiamato quando Aspose.Words salva una pagina separata in formati di pagina fissi.

```csharp
public void PageSaving(PageSavingArgs args)
```

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

* class [PageSavingArgs](../../pagesavingargs/)
* interface [IPageSavingCallback](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
