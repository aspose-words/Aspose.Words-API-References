---
title: PageSavingArgs.KeepPageStreamOpen
linktitle: KeepPageStreamOpen
articleTitle: KeepPageStreamOpen
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété KeepPageStreamOpen dans PageSavingArgs améliore la gestion des documents avec Aspose.Words en contrôlant le comportement du flux pour des performances optimales.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/pagesavingargs/keeppagestreamopen/
---
## PageSavingArgs.KeepPageStreamOpen property

Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une page de document.

```csharp
public bool KeepPageStreamOpen { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` et Aspose.Words fermera le flux que vous avez fourni dans le[`PageStream`](../pagestream/) propriété après avoir écrit une page de document dedans. Spécifier`vrai` pour garder le ruisseau ouvert.

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

* class [PageSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
