---
title: IPageSavingCallback Interface
linktitle: IPageSavingCallback
articleTitle: IPageSavingCallback
second_title: Aspose.Words pour .NET
description: Contrôlez l'enregistrement des documents avec Aspose.Words.Saving.IPageSavingCallback. Personnalisez l'enregistrement des pages dans des formats fixes pour des résultats optimaux.
type: docs
weight: 5930
url: /fr/net/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface

Implémentez cette interface si vous souhaitez contrôler la manière dont Aspose.Words enregistre des pages séparées lors de l'enregistrement d'un document dans des formats de page fixes.

```csharp
public interface IPageSavingCallback
```

## Méthodes

| Nom | La description |
| --- | --- |
| [PageSaving](../../aspose.words.saving/ipagesavingcallback/pagesaving/)(*[PageSavingArgs](../pagesavingargs/)*) | Appelé lorsque Aspose.Words enregistre une page distincte dans des formats de page fixes. |

## Exemples

Montre comment utiliser un rappel pour enregistrer un document au format HTML page par page.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Créez un objet « HtmlFixedSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
    // pour modifier la façon dont nous convertissons le document en HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Nous enregistrerons chaque page de ce document dans un fichier HTML distinct dans le système de fichiers local.
    // Définissez un rappel qui nous permet de nommer chaque document HTML de sortie.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Enregistre toutes les pages dans un fichier et un répertoire spécifiés à l'intérieur.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Vous trouverez ci-dessous deux manières de spécifier où Aspose.Words enregistrera chaque page du document.
        // 1 - Définir un nom de fichier pour le fichier de page de sortie :
        args.PageFileName = outFileName;

        // 2 - Créer un flux personnalisé pour le fichier de page de sortie :
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
