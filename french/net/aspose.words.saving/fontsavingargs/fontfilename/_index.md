---
title: FontSavingArgs.FontFileName
second_title: Référence de l'API Aspose.Words pour .NET
description: FontSavingArgs propriété. Obtient ou définit le nom du fichier sans chemin dans lequel la police sera enregistrée.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Obtient ou définit le nom du fichier (sans chemin) dans lequel la police sera enregistrée.

```csharp
public string FontFileName { get; set; }
```

### Remarques

Cette propriété vous permet de redéfinir la façon dont les noms de fichiers de police sont générés lors de l'exportation vers HTML.

Lorsque l'événement est déclenché, cette propriété contient le nom de fichier qui a été généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer la police dans un fichier différent . Notez que les noms de fichiers doivent être uniques.

Aspose.Words génère automatiquement un nom de fichier unique pour chaque police intégrée lors de l'exportation au format HTML. La façon dont le nom du fichier de police est généré dépend si vous enregistrez le document dans un fichier ou dans un flux.

Lors de l'enregistrement d'un document dans un fichier, le nom du fichier de police généré ressemble à &lt;nom du fichier de base du document&gt;.&lt;nom du fichier d'origine&gt;&lt;suffixe facultatif&gt;.&lt;extension&gt;.

Lors de l'enregistrement d'un document dans un flux, le nom du fichier de police généré ressemble à Aspose.Words.&lt;guid du document&gt;.&lt;nom du fichier d'origine&gt;&lt;suffixe facultatif&gt;.&lt;extension&gt;.

`FontFileName` doit contenir uniquement le nom du fichier sans le chemin. Aspose.Words détermine le chemin d'enregistrement à l'aide du nom du fichier du document, le[`FontsFolder`](../../htmlsaveoptions/fontsfolder/) et [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) Propriétés.

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

* class [FontSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../fontsavingargs/)
* Assemblée [Aspose.Words](../../../)


