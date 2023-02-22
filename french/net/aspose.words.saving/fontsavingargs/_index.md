---
title: Class FontSavingArgs
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.FontSavingArgs classe. Fournit des données pour leFontSaving événement.
type: docs
weight: 4770
url: /fr/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Fournit des données pour le[`FontSaving`](../ifontsavingcallback/fontsaving/) événement.

```csharp
public class FontSavingArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Indique si la police actuelle est en gras. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Obtient l'objet document en cours d'enregistrement. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Indique le nom de la famille de polices actuelle. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Obtient ou définit le nom du fichier (sans chemin) dans lequel la police sera enregistrée. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Permet de spécifier le flux dans lequel la police sera enregistrée. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Permet de spécifier si la police courante sera exportée en tant que ressource de police. La valeur par défaut est`vrai` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Permet de spécifier si la police actuelle sera sous-ensemble avant d'exporter en tant que ressource de police. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Indique si la police actuelle est en italique. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après avoir enregistré une police. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Obtient le nom du fichier de police d'origine avec une extension. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Obtient la taille du fichier de police d'origine. |

### Remarques

Lorsque Aspose.Words enregistre un document au format HTML ou aux formats associés et[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) est défini sur **vrai**, il enregistre chaque sujet de police pour l'exportation dans un fichier séparé.

`FontSavingArgs` contrôle si une ressource de police particulière doit être exportée et comment.

`FontSavingArgs`permet également de redéfinir la façon dont les noms de fichiers de polices sont générés ou de contourner complètement l'enregistrement des polices dans des fichiers en fournissant vos propres objets de flux.

Pour décider d'enregistrer ou non une ressource de police particulière, utilisez la[`IsExportNeeded`](./isexportneeded/) propriété.

Pour enregistrer les polices dans des flux au lieu de fichiers, utilisez la[`FontStream`](./fontstream/) propriété.

### Exemples

Montre comment définir une logique personnalisée pour l'exportation des polices lors de l'enregistrement au format HTML.

```csharp
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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


