---
title: ImageSavingArgs.ImageFileName
second_title: Référence de l'API Aspose.Words pour .NET
description: ImageSavingArgs propriété. Obtient ou définit le nom du fichier sans chemin dans lequel limage sera enregistrée.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/imagesavingargs/imagefilename/
---
## ImageSavingArgs.ImageFileName property

Obtient ou définit le nom du fichier (sans chemin) dans lequel l'image sera enregistrée.

```csharp
public string ImageFileName { get; set; }
```

### Remarques

Cette propriété permet de redéfinir la façon dont les noms de fichiers image sont générés lors de l'export au format HTML.

Lorsque l'événement est déclenché, cette propriété contient le nom de fichier généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer l'image dans un fichier différent. Notez que les noms de fichiers doivent être uniques.

Aspose.Words génère automatiquement un nom de fichier unique pour chaque image intégrée lors de l'exportation au format HTML. La façon dont le nom du fichier image est généré dépend du fait que vous enregistrez le document dans un fichier ou dans un flux.

Lors de l'enregistrement d'un document dans un fichier, le nom du fichier image généré ressemble à &lt;nom du fichier de base du document&gt;.&lt;numéro d'image&gt;.&lt;extension&gt;.

Lors de l'enregistrement d'un document dans un flux, le nom du fichier image généré ressemble à Aspose.Words.&lt;guid du document&gt;.&lt;numéro d'image&gt;.&lt;extension&gt;.

`ImageFileName` doit contenir uniquement le nom du fichier sans le chemin. Aspose.Words détermine le chemin de sauvegarde et la valeur du`src` attribut pour écrire en HTML en utilisant le nom du fichier du document, le[`ImagesFolder`](../../htmlsaveoptions/imagesfolder/) et [`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias/) propriétés.

### Exemples

Montre comment diviser un document en parties et les enregistrer.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crée un objet "HtmlFixedSaveOptions", que l'on peut passer à la méthode "Save" du document
    // pour modifier la façon dont nous convertissons le document en HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si nous enregistrons le document normalement, il y aura une sortie HTML
    // document avec tout le contenu du document source.
    // Définissez la propriété "DocumentSplitCriteria" sur "DocumentSplitCriteria.SectionBreak" pour
    // enregistre notre document dans plusieurs fichiers HTML : un pour chaque section.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Attribuez un rappel personnalisé à la propriété "DocumentPartSavingCallback" pour modifier la logique d'enregistrement des parties du document.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si nous convertissons un document contenant des images en HTML, nous nous retrouverons avec un fichier HTML qui renvoie à plusieurs images.
    // Chaque image sera sous la forme d'un fichier dans le système de fichiers local.
    // Il existe également un rappel qui permet de personnaliser le nom et l'emplacement du système de fichiers de chaque image.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Définit des noms de fichiers personnalisés pour les documents de sortie dans lesquels l'opération d'enregistrement divise un document.
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
        // On peut accéder à l'intégralité du document source via la propriété "Document".
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

        // Vous trouverez ci-dessous deux manières de spécifier où Aspose.Words enregistrera chaque partie du document.
        // 1 - Définissez un nom de fichier pour le fichier pièce de sortie :
        args.DocumentPartFileName = partFileName;

        // 2 - Créez un flux personnalisé pour le fichier pièce de sortie :
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Définit des noms de fichiers personnalisés pour les fichiers image créés par une conversion HTML.
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

        // Vous trouverez ci-dessous deux manières de spécifier où Aspose.Words enregistrera chaque partie du document.
        // 1 - Définissez un nom de fichier pour le fichier image de sortie :
        args.ImageFileName = imageFileName;

        // 2 - Créez un flux personnalisé pour le fichier image de sortie :
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

* class [ImageSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../imagesavingargs/)
* Assemblée [Aspose.Words](../../../)


