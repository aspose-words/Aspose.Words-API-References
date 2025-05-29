---
title: MarkdownSaveOptions.ImageSavingCallback
linktitle: ImageSavingCallback
articleTitle: ImageSavingCallback
second_title: Aspose.Words per .NET
description: Controlla il salvataggio delle immagini in Markdown con ImageSavingCallback di MarkdownSaveOptions. Migliora la formattazione dei documenti e semplifica il tuo flusso di lavoro senza sforzo!
type: docs
weight: 70
url: /it/net/aspose.words.saving/markdownsaveoptions/imagesavingcallback/
---
## MarkdownSaveOptions.ImageSavingCallback property

Consente di controllare come vengono salvate le immagini quando un documento viene salvato su Markdown formato.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
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

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
