---
title: Interface IPageSavingCallback
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.IPageSavingCallback interfaccia. Implementa questa interfaccia se vuoi controllare come Aspose.Words salva pagine separate quando salva un documento in formati di pagina fissi.
type: docs
weight: 4920
url: /it/net/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface

Implementa questa interfaccia se vuoi controllare come Aspose.Words salva pagine separate quando salva un documento in formati di pagina fissi.

```csharp
public interface IPageSavingCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [PageSaving](../../aspose.words.saving/ipagesavingcallback/pagesaving/)(PageSavingArgs) | Chiamato quando Aspose.Words salva una pagina separata in formati di pagina fissi. |

### Esempi

Mostra come utilizzare una richiamata per salvare un documento in HTML pagina per pagina.

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
    // Imposta un callback che ci permetta di denominare ogni documento HTML di output.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Salva tutte le pagine in un file e in una directory specificati all'interno.
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


