---
title: FixedPageSaveOptions.PageSavingCallback
linktitle: PageSavingCallback
articleTitle: PageSavingCallback
second_title: Aspose.Words pour .NET
description: Contrôlez l'enregistrement des pages avec PageSavingCallback de FixedPageSaveOptions. Optimisez l'exportation de documents vers des formats fixes pour une efficacité et une précision accrues.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/
---
## FixedPageSaveOptions.PageSavingCallback property

Permet de contrôler la manière dont les pages séparées sont enregistrées lorsqu'un document est exporté vers un format de page fixe.

```csharp
public IPageSavingCallback PageSavingCallback { get; set; }
```

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

* interface [IPageSavingCallback](../../ipagesavingcallback/)
* class [FixedPageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
