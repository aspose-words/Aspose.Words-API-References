---
title: ImageSavingArgs Class
linktitle: ImageSavingArgs
articleTitle: ImageSavingArgs
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.ImageSavingArgs classe. Fornisce i dati per ilImageSaving evento in C#.
type: docs
weight: 5240
url: /it/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Fornisce i dati per il[`ImageSaving`](../iimagesavingcallback/imagesaving/) evento.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class ImageSavingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Ottiene il file[`ShapeBase`](../../aspose.words.drawing/shapebase/) oggetto corrispondente alla forma o alla forma del gruppo che sta per essere salvato. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Ottiene l'oggetto documento attualmente in fase di salvataggio. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Ottiene o imposta il nome del file (senza percorso) in cui verrà salvata l'immagine. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Permette di specificare lo stream in cui verrà salvata l'immagine. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | Restituisce`VERO` se l'immagine corrente è disponibile per l'esportazione. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Specifica se Aspose.Words deve mantenere aperto lo stream o chiuderlo dopo aver salvato un'immagine. |

## Osservazioni

Per impostazione predefinita, quando Aspose.Words salva un documento in HTML, salva ogni immagine in un file separato. Aspose.Words utilizza il nome del file del documento e un numero univoco per generare un nome file univoco per ogni immagine trovata nel documento.

`ImageSavingArgs`consente di ridefinire il modo in cui vengono generati i nomi dei file di immagine o di aggirare completamente il salvataggio delle immagini nei file fornendo i propri oggetti stream.

Per applicare la tua logica per generare nomi di file immagine, utilizza [`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) E[`IsImageAvailable`](./isimageavailable/) proprietà .

Per salvare le immagini in flussi anziché in file, utilizzare il file[`ImageStream`](./imagestream/) proprietà.

## Esempi

Mostra come dividere un documento in parti e salvarle.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crea un oggetto "HtmlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui convertiamo il documento in HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Se salviamo il documento normalmente, ci sarà un output HTML
    // documento con tutto il contenuto del documento sorgente.
    // Imposta la proprietà "DocumentSplitCriteria" su "DocumentSplitCriteria.SectionBreak" su
    // salva il nostro documento in più file HTML: uno per ogni sezione.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Assegna un callback personalizzato alla proprietà "DocumentPartSavingCallback" per modificare la logica di salvataggio della parte del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Se convertiamo un documento che contiene immagini in html, ci ritroveremo con un file html che collega a diverse immagini.
    // Ogni immagine avrà la forma di un file nel file system locale.
    // Esiste anche un callback che può personalizzare il nome e la posizione del file system di ciascuna immagine.
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
        // Possiamo accedere all'intero documento sorgente tramite la proprietà "Document".
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
