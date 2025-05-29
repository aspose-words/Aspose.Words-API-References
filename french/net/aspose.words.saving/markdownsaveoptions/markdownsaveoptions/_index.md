---
title: MarkdownSaveOptions
linktitle: MarkdownSaveOptions
articleTitle: MarkdownSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur MarkdownSaveOptions pour enregistrer facilement vos documents au format Markdown. Optimisez votre flux de travail grâce à cet outil essentiel.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/markdownsaveoptions/markdownsaveoptions/
---
## MarkdownSaveOptions constructor

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leMarkdown format.

```csharp
public MarkdownSaveOptions()
```

## Exemples

Montre comment renommer le nom de l'image lors de l'enregistrement dans un document Markdown.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Si nous convertissons un document contenant des images en Markdown, nous nous retrouverons avec un fichier Markdown contenant des liens vers plusieurs images.
    // Chaque image sera sous la forme d'un fichier dans le système de fichiers local.
    // Il existe également un rappel qui peut personnaliser le nom et l'emplacement du système de fichiers de chaque image.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // La méthode ImageSaving() de notre rappel sera exécutée à ce moment.
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
/// Renomme les images enregistrées qui sont produites lors de l'enregistrement d'un document Markdown.
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

### Voir également

* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
