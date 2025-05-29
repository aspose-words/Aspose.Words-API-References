---
title: IImageSavingCallback Interface
linktitle: IImageSavingCallback
articleTitle: IImageSavingCallback
second_title: Aspose.Words per .NET
description: Controlla il salvataggio delle immagini in Aspose.Words con l'interfaccia IImageSavingCallback. Ottimizza le esportazioni dei documenti in HTML e altri formati senza sforzo.
type: docs
weight: 5920
url: /it/net/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface

Implementa questa interfaccia se vuoi controllare come Aspose.Words salva le immagini quando salva un documento in HTML. Può essere utilizzata anche da altri formati.

```csharp
public interface IImageSavingCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ImageSaving](../../aspose.words.saving/iimagesavingcallback/imagesaving/)(*[ImageSavingArgs](../imagesavingargs/)*) | Chiamato quando Aspose.Words salva un'immagine in HTML. |

## Esempi

Mostra come rinominare l'immagine durante il salvataggio nel documento Markdown.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Se convertiamo in Markdown un documento contenente immagini, otterremo un file Markdown che rimanda a più immagini.
    // Ogni immagine sarà sotto forma di file nel file system locale.
    // Esiste anche una callback che può personalizzare il nome e la posizione del file system di ciascuna immagine.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // In questo momento verrà eseguito il metodo ImageSaving() del nostro callback.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// Rinomina le immagini salvate prodotte quando si salva un documento Markdown.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        args.ImageFileName = imageFileName;
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

Mostra come dividere un documento in parti e salvarle.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Creiamo un oggetto "HtmlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui convertiamo il documento in HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Se salviamo il documento normalmente, ci sarà un output HTML
    // documento con tutto il contenuto del documento sorgente.
    // Imposta la proprietà "DocumentSplitCriteria" su "DocumentSplitCriteria.SectionBreak" per
    // salviamo il nostro documento in più file HTML: uno per ogni sezione.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Assegna un callback personalizzato alla proprietà "DocumentPartSavingCallback" per modificare la logica di salvataggio delle parti del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Se convertiamo in HTML un documento contenente immagini, otterremo un file HTML contenente collegamenti a più immagini.
    // Ogni immagine sarà sotto forma di file nel file system locale.
    // Esiste anche una callback che può personalizzare il nome e la posizione del file system di ciascuna immagine.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Imposta nomi di file personalizzati per i documenti di output in cui l'operazione di salvataggio suddivide un documento.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Possiamo accedere all'intero documento sorgente tramite la proprietà "Documento".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Di seguito sono riportati due modi per specificare dove Aspose.Words salverà ciascuna parte del documento.
        // 1 - Imposta un nome file per il file di output:
        args.DocumentPartFileName = partFileName;

        // 2 - Crea un flusso personalizzato per il file di output:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Imposta nomi di file personalizzati per i file immagine creati da una conversione HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Di seguito sono riportati due modi per specificare dove Aspose.Words salverà ciascuna parte del documento.
        // 1 - Imposta un nome file per il file immagine di output:
        args.ImageFileName = imageFileName;

        // 2 - Crea un flusso personalizzato per il file immagine di output:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
