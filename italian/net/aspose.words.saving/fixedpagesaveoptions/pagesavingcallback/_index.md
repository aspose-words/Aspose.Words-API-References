---
title: FixedPageSaveOptions.PageSavingCallback
second_title: Aspose.Words per .NET API Reference
description: FixedPageSaveOptions proprietà. Permette di controllare come vengono salvate le pagine separate quando un documento viene esportato in un formato di pagina fisso.
type: docs
weight: 60
url: /it/net/aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/
---
## FixedPageSaveOptions.PageSavingCallback property

Permette di controllare come vengono salvate le pagine separate quando un documento viene esportato in un formato di pagina fisso.

```csharp
public IPageSavingCallback PageSavingCallback { get; set; }
```

### Esempi

Mostra come utilizzare un callback per salvare un documento in HTML pagina per pagina.

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

    // Crea un oggetto "HtmlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui convertiamo il documento in HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Salveremo ogni pagina di questo documento in un file HTML separato nel file system locale.
    // Imposta un callback che ci permette di nominare ogni documento HTML di output.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Salva tutte le pagine in un file e in una directory specificata all'interno.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Di seguito sono riportati due modi per specificare dove Aspose.Words salverà ogni pagina del documento.
        // 1 - Imposta un nome file per il file della pagina di output:
        args.PageFileName = outFileName;

        // 2 - Crea un flusso personalizzato per il file della pagina di output:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Guarda anche

* interface [IPageSavingCallback](../../ipagesavingcallback/)
* class [FixedPageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* assemblea [Aspose.Words](../../../)


