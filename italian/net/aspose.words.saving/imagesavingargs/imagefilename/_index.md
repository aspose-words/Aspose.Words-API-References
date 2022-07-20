---
title: ImageFileName
second_title: Aspose.Words per .NET API Reference
description: Ottiene o imposta il nome del file senza percorso in cui verrà salvata limmagine.
type: docs
weight: 30
url: /it/net/aspose.words.saving/imagesavingargs/imagefilename/
---
## ImageSavingArgs.ImageFileName property

Ottiene o imposta il nome del file (senza percorso) in cui verrà salvata l'immagine.

```csharp
public string ImageFileName { get; set; }
```

### Osservazioni

Questa proprietà consente di ridefinire il modo in cui i nomi dei file di immagine vengono generati durante l'esportazione in HTML.

Quando l'evento viene generato, questa proprietà contiene il nome del file che è stato generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare l'immagine in un file diverso. Tieni presente che i nomi dei file devono essere univoci.

Aspose.Words genera automaticamente un nome file univoco per ogni immagine incorporata durante l'esportazione di in formato HTML. Il modo in cui viene generato il nome del file immagine dipende dal fatto che il documento venga salvato in un file o in un flusso.

Quando si salva un documento in un file, il nome del file immagine generato è simile a &lt;nome file base documento&gt;.&lt;numero immagine&gt;.&lt;estensione&gt;.

Quando si salva un documento in uno stream, il nome del file di immagine generato è simile a Aspose.Words.&lt;documento guida&gt;.&lt;numero immagine&gt;.&lt;estensione&gt;.

`ImageFileName` deve contenere solo il nome del file senza il percorso. Aspose.Words determina il percorso per il salvataggio e il valore del`src`attributo per scrivere in HTML utilizzando il nome del file del documento, il[`ImagesFolder`](../../htmlsaveoptions/imagesfolder) e [`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias) proprietà.

### Esempi

Mostra come dividere un documento in parti e salvarle.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crea un oggetto "HtmlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui convertiamo il documento in HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Se salviamo il documento normalmente, ci sarà un HTML di output
    // documento con tutti i contenuti del documento sorgente.
    // Imposta la proprietà "DocumentSplitCriteria" su "DocumentSplitCriteria.SectionBreak" su
    // salva il nostro documento in più file HTML: uno per ogni sezione.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Assegna un callback personalizzato alla proprietà "DocumentPartSavingCallback" per modificare la logica di salvataggio della parte del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Se convertiamo un documento che contiene immagini in html, ci ritroveremo con un file html che si collega a più immagini.
    // Ogni immagine avrà la forma di un file nel file system locale.
    // C'è anche un callback che può personalizzare il nome e la posizione del file system di ogni immagine.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Imposta nomi di file personalizzati per i documenti di output in cui l'operazione di salvataggio divide un documento.
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

        // Di seguito sono riportati due modi per specificare dove Aspose.Words salverà ogni parte del documento.
        // 1 - Imposta un nome file per il file della parte di output:
        args.DocumentPartFileName = partFileName;

        // 2 - Crea un flusso personalizzato per il file della parte di output:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Imposta nomi di file personalizzati per i file di immagine creati da una conversione HTML.
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

        // Di seguito sono riportati due modi per specificare dove Aspose.Words salverà ogni parte del documento.
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

* class [ImageSavingArgs](../../imagesavingargs)
* spazio dei nomi [Aspose.Words.Saving](../../imagesavingargs)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->