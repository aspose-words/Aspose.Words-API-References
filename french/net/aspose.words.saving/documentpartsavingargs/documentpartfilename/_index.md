---
title: DocumentPartFileName
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit le nom du fichier sans chemin dans lequel la partie du document sera enregistrée.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/documentpartsavingargs/documentpartfilename/
---
## DocumentPartSavingArgs.DocumentPartFileName property

Obtient ou définit le nom du fichier (sans chemin) dans lequel la partie du document sera enregistrée.

```csharp
public string DocumentPartFileName { get; set; }
```

### Remarques

Cette propriété vous permet de redéfinir la façon dont les noms de fichier de partie de document sont générés lors de l'exportation vers HTML ou EPUB.

Lorsque le rappel est appelé, cette propriété contient le nom de fichier qui a été généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer la partie du document dans un fichier différent . Notez que le nom de fichier de chaque pièce doit être unique.

`DocumentPartFileName` doit contenir uniquement le nom du fichier sans le chemin. Aspose.Words détermine le chemin d'enregistrement à l'aide du nom de fichier du document. Si le nom de fichier du document de sortie n'a pas été spécifié, par exemple lors de l'enregistrement dans un flux, ce nom de fichier est utilisé uniquement pour référencer les parties du document. Il en va de même lors de l'enregistrement au format EPUB.

### Exemples

Montre comment diviser un document en plusieurs parties et les enregistrer.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crée un objet "HtmlFixedSaveOptions", que nous pouvons passer à la méthode "Save" du document
    // pour modifier la façon dont nous convertissons le document en HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si nous enregistrons le document normalement, il y aura une sortie HTML
    // document avec tout le contenu du document source.
    // Définissez la propriété "DocumentSplitCriteria" sur "DocumentSplitCriteria.SectionBreak" pour
    // enregistre notre document dans plusieurs fichiers HTML : un pour chaque section.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Attribuez un rappel personnalisé à la propriété "DocumentPartSavingCallback" pour modifier la logique d'enregistrement de la partie du document.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si nous convertissons un document contenant des images en html, nous nous retrouverons avec un fichier html qui renvoie à plusieurs images.
    // Chaque image sera sous la forme d'un fichier dans le système de fichiers local.
    // Il existe également un rappel qui peut personnaliser le nom et l'emplacement du système de fichiers de chaque image.
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
        // Nous pouvons accéder à l'intégralité du document source via la propriété "Document".
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
        // 1 - Définissez un nom de fichier pour le fichier partiel de sortie :
        args.DocumentPartFileName = partFileName;

        // 2 - Créez un flux personnalisé pour le fichier partiel de sortie :
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

* class [DocumentPartSavingArgs](../../documentpartsavingargs)
* espace de noms [Aspose.Words.Saving](../../documentpartsavingargs)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
