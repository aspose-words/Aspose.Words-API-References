---
title: FontSavingArgs.KeepFontStreamOpen
linktitle: KeepFontStreamOpen
articleTitle: KeepFontStreamOpen
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété KeepFontStreamOpen dans FontSavingArgs permet à Aspose.Words de gérer efficacement les flux de polices, améliorant ainsi votre expérience de traitement de documents.
type: docs
weight: 90
url: /fr/net/aspose.words.saving/fontsavingargs/keepfontstreamopen/
---
## FontSavingArgs.KeepFontStreamOpen property

Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une police.

```csharp
public bool KeepFontStreamOpen { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` et Aspose.Words fermera le flux que vous avez fourni dans le[`FontStream`](../fontstream/) propriété après avoir écrit une police dedans. Spécifier`vrai` pour garder le ruisseau ouvert.

## Exemples

Montre comment définir une logique personnalisée pour l'exportation de polices lors de l'enregistrement au format HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Configurez un objet SaveOptions pour exporter les polices vers des fichiers séparés.
    // Définissez un rappel qui gérera l'enregistrement des polices de manière personnalisée.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Le rappel exportera les fichiers .ttf et les enregistrera avec le document de sortie.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Imprime des informations sur les polices exportées et les enregistre dans le même dossier système local que leur sortie .html.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Nous pouvons également accéder au document source à partir d'ici.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Il existe deux manières d'enregistrer une police exportée.
        // 1 - Enregistrez-le dans un emplacement du système de fichiers local :
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Enregistrez-le dans un flux :
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Voir également

* class [FontSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
