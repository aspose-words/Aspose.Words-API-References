---
title: PageSavingArgs Class
linktitle: PageSavingArgs
articleTitle: PageSavingArgs
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.PageSavingArgs, essentielle pour optimiser le traitement des documents grâce à des données détaillées sur les événements PageSaving. Améliorez votre flux de travail !
type: docs
weight: 6160
url: /fr/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

Fournit des données pour le[`PageSaving`](../ipagesavingcallback/pagesaving/) événement.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public class PageSavingArgs
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PageSavingArgs](pagesavingargs/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une page de document. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | Obtient ou définit le nom du fichier dans lequel la page du document sera enregistrée. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | Index de la page actuelle. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | Permet de spécifier le flux dans lequel la page du document sera enregistrée. |

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
