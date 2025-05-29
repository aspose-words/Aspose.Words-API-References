---
title: DocumentPartSavingArgs Class
linktitle: DocumentPartSavingArgs
articleTitle: DocumentPartSavingArgs
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.DocumentPartSavingArgs, essentielle pour améliorer le traitement des documents avec des options de sauvegarde personnalisables et des rappels efficaces.
type: docs
weight: 5690
url: /fr/net/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class

Fournit des données pour le[`DocumentPartSaving`](../idocumentpartsavingcallback/documentpartsaving/) rappel.

Pour en savoir plus, visitez le[Enregistrer un document](https://docs.aspose.com/words/net/save-a-document/) article de documentation.

```csharp
public class DocumentPartSavingArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Document](../../aspose.words.saving/documentpartsavingargs/document/) { get; } | Obtient l'objet document en cours d'enregistrement. |
| [DocumentPartFileName](../../aspose.words.saving/documentpartsavingargs/documentpartfilename/) { get; set; } | Obtient ou définit le nom du fichier (sans chemin) dans lequel la partie du document sera enregistrée. |
| [DocumentPartStream](../../aspose.words.saving/documentpartsavingargs/documentpartstream/) { get; set; } | Permet de spécifier le flux dans lequel la partie du document sera enregistrée. |
| [KeepDocumentPartStreamOpen](../../aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/) { get; set; } | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une partie du document. |

## Remarques

Lorsque Aspose.Words enregistre un document au format HTML ou dans des formats associés et[`DocumentSplitCriteria`](../htmlsaveoptions/documentsplitcriteria/) est spécifié, le document est divisé en parties et par défaut, chaque partie du document est enregistrée dans un fichier séparé.

Classe`DocumentPartSavingArgs` vous permet de contrôler la manière dont chaque partie du document sera enregistrée. Il permet de redéfinir la manière dont les noms de fichiers sont générés ou de contourner complètement l'enregistrement des parties du document dans des fichiers en fournissant vos propres objets de flux.

Pour enregistrer des parties de document dans des flux plutôt que dans des fichiers, utilisez le[`DocumentPartStream`](./documentpartstream/) propriété.

## Exemples

Montre comment diviser un document en parties et les enregistrer.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Créez un objet « HtmlFixedSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
    // pour modifier la façon dont nous convertissons le document en HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si nous enregistrons le document normalement, il y aura un seul HTML de sortie
    // document avec tout le contenu du document source.
    // Définissez la propriété « DocumentSplitCriteria » sur « DocumentSplitCriteria.SectionBreak » pour
    // enregistrez notre document dans plusieurs fichiers HTML : un pour chaque section.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Affectez un rappel personnalisé à la propriété « DocumentPartSavingCallback » pour modifier la logique d'enregistrement de la partie du document.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si nous convertissons un document contenant des images en HTML, nous nous retrouverons avec un fichier HTML contenant des liens vers plusieurs images.
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
        // 1 - Définir un nom de fichier pour le fichier de sortie :
        args.DocumentPartFileName = partFileName;

        // 2 - Créer un flux personnalisé pour le fichier de sortie :
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
        // 1 - Définir un nom de fichier pour le fichier image de sortie :
        args.ImageFileName = imageFileName;

        // 2 - Créer un flux personnalisé pour le fichier image de sortie :
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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
