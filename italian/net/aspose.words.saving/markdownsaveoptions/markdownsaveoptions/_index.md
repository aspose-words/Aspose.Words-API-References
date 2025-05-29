---
title: MarkdownSaveOptions
linktitle: MarkdownSaveOptions
articleTitle: MarkdownSaveOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore MarkdownSaveOptions per salvare facilmente i documenti in formato Markdown. Semplifica il tuo flusso di lavoro con questo strumento essenziale.
type: docs
weight: 10
url: /it/net/aspose.words.saving/markdownsaveoptions/markdownsaveoptions/
---
## MarkdownSaveOptions constructor

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nelMarkdown formato.

```csharp
public MarkdownSaveOptions()
```

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

### Guarda anche

* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
