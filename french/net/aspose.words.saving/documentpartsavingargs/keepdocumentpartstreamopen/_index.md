---
title: DocumentPartSavingArgs.KeepDocumentPartStreamOpen
linktitle: KeepDocumentPartStreamOpen
articleTitle: KeepDocumentPartStreamOpen
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété KeepDocumentPartStreamOpen dans DocumentPartSavingArgs permet à Aspose.Words de gérer efficacement les flux de parties de documents pour des performances optimales.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs.KeepDocumentPartStreamOpen property

Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une partie du document.

```csharp
public bool KeepDocumentPartStreamOpen { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` et Aspose.Words fermera le flux que vous avez fourni dans le[`DocumentPartStream`](../documentpartstream/) propriété après avoir écrit une partie du document dedans. Spécifier`vrai` pour maintenir le flux ouvert. Veuillez noter que le flux de sortie principal fourni dans l'appel à[`Save`](../../../aspose.words/document/save/)ou [`Save`](../../../aspose.words/document/save/) ne sera jamais fermé par Aspose.Words même si`KeepDocumentPartStreamOpen` est réglé sur`FAUX`.

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

* class [DocumentPartSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
