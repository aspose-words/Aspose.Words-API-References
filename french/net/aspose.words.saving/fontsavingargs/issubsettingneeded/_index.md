---
title: FontSavingArgs.IsSubsettingNeeded
linktitle: IsSubsettingNeeded
articleTitle: IsSubsettingNeeded
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FontSavingArgs IsSubsettingNeeded pour contrôler le sous-ensemble des polices et optimiser l'exportation de vos ressources. Améliorez votre processus de création dès aujourd'hui !
type: docs
weight: 70
url: /fr/net/aspose.words.saving/fontsavingargs/issubsettingneeded/
---
## FontSavingArgs.IsSubsettingNeeded property

Permet de spécifier si la police actuelle sera sous-ensemble avant d'être exportée en tant que ressource de police.

```csharp
public bool IsSubsettingNeeded { get; set; }
```

## Remarques

Les polices peuvent être exportées sous forme de fichiers originaux complets ou sous-ensembles pour n'inclure que les caractères utilisés dans le document. Le sous-ensemble permet de réduire la taille des ressources de polices obtenues.

Par défaut, Aspose.Words décide d'effectuer ou non un sous-ensemble en comparant la taille du fichier de police d'origine avec celle spécifiée dans[`FontResourcesSubsettingSizeThreshold`](../../htmlsaveoptions/fontresourcessubsettingsizethreshold/) . Vous pouvez remplacer ce comportement pour des polices individuelles en définissant le`IsSubsettingNeeded` propriété.

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
