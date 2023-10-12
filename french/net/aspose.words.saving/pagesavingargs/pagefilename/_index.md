---
title: PageSavingArgs.PageFileName
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSavingArgs propriété. Obtient ou définit le nom du fichier dans lequel la page du document sera enregistrée.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pagesavingargs/pagefilename/
---
## PageSavingArgs.PageFileName property

Obtient ou définit le nom du fichier dans lequel la page du document sera enregistrée.

```csharp
public string PageFileName { get; set; }
```

### Remarques

S'il n'est pas spécifié, le nom et le chemin du fichier d'échange seront générés automatiquement en utilisant le nom du fichier d'origine.

### Exemples

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

    // Crée un objet "HtmlFixedSaveOptions", que l'on peut passer à la méthode "Save" du document
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

        // Vous trouverez ci-dessous deux façons de spécifier où Aspose.Words enregistrera chaque page du document.
        // 1 - Définissez un nom de fichier pour le fichier d'échange de sortie :
        args.PageFileName = outFileName;

        // 2 - Créez un flux personnalisé pour le fichier d'échange de sortie :
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Voir également

* class [PageSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../pagesavingargs/)
* Assemblée [Aspose.Words](../../../)


