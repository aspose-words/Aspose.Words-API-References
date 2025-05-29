---
title: DocumentPartSavingArgs.DocumentPartStream
linktitle: DocumentPartStream
articleTitle: DocumentPartStream
second_title: Aspose.Words per .NET
description: Scopri come la proprietà DocumentPartStream in DocumentPartSavingArgs ti consente di specificare facilmente dove salvare le parti del documento per una gestione ottimale.
type: docs
weight: 30
url: /it/net/aspose.words.saving/documentpartsavingargs/documentpartstream/
---
## DocumentPartSavingArgs.DocumentPartStream property

Consente di specificare il flusso in cui verrà salvata la parte del documento.

```csharp
public Stream DocumentPartStream { get; set; }
```

## Osservazioni

Questa proprietà consente di salvare parti di documenti in flussi anziché in file durante l'esportazione HTML.

Il valore predefinito è`null` Quando questa proprietà è`null` , la parte del documento verrà salvata in un file specificato nel[`DocumentPartFileName`](../documentpartfilename/) proprietà.

Quando viene richiesto il salvataggio in un flusso in formato HTML[`Save`](../../../aspose.words/document/save/) o[`Save`](../../../aspose.words/document/save/) e la prima parte del documento sta per essere salvata, Aspose.Words suggerisce qui il flusso di output principale inizialmente passato dal chiamante.

Quando si salva in formato EPUB, che è un formato contenitore basato su HTML,`DocumentPartStream` non è possibile specificare perché tutte le parti sussidiarie verranno incapsulate in un singolo pacchetto di output.

## Esempi

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

* class [DocumentPartSavingArgs](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
