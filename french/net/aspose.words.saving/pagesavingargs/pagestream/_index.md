---
title: PageSavingArgs.PageStream
linktitle: PageStream
articleTitle: PageStream
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageStream de PageSavingArgs, permettant un enregistrement transparent des pages de document dans le flux souhaité pour une gestion efficace des fichiers.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/pagesavingargs/pagestream/
---
## PageSavingArgs.PageStream property

Permet de spécifier le flux dans lequel la page du document sera enregistrée.

```csharp
public Stream PageStream { get; set; }
```

## Remarques

Cette propriété vous permet d'enregistrer des pages de document dans des flux plutôt que dans des fichiers.

La valeur par défaut est`nul` . Lorsque cette propriété est`nul` , la page du document sera enregistrée dans un fichier spécifié dans le[`PageFileName`](../pagefilename/) propriété.

Si les deux`PageStream` et[`PageFileName`](../pagefilename/) sont définis, alors PageStream sera utilisé.

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
