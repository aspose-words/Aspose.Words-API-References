---
title: HtmlSaveOptions.ExportFontResources
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Spécifie si les ressources de polices doivent être exportées au format HTML MHTML ou EPUB. La valeur par défaut estFAUX .
type: docs
weight: 140
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Spécifie si les ressources de polices doivent être exportées au format HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool ExportFontResources { get; set; }
```

### Remarques

L'exportation de ressources de polices permet un rendu cohérent des documents, indépendamment des polices disponibles dans l'environnement d'un utilisateur donné.

Si`ExportFontResources` est réglé sur`vrai` , le document HTML principal fera référence à chaque police via le CSS 3 **@font-face** La règle at et les polices seront sorties sous forme de fichiers séparés. Lors de l'exportation aux formats IDPF EPUB ou MHTML , les polices seront intégrées dans le package correspondant avec d'autres fichiers subsidiaires.

Si[`ExportFontsAsBase64`](../exportfontsasbase64/) est réglé sur`vrai` les polices ne seront pas enregistrées dans des fichiers séparés. Au lieu de cela, elles seront intégrées dans **@font-face** règles at dans l'encodage Base64.

**Important!** Lors de l’exportation de ressources de polices, les problèmes de licence de polices doivent être pris en compte. Les auteurs qui souhaitent utiliser des polices spécifiques via un mécanisme de police downloadable doivent toujours vérifier soigneusement que leur utilisation prévue entre dans le cadre de la licence de police. De nombreuses polices commerciales ne permettent actuellement pas de télécharger leurs polices sur le Web sous quelque forme que ce soit. Les contrats de licence qui couvrent certaines polices indiquent spécifiquement que l'utilisation via **@font-face** Rules dans les feuilles de style CSS n'est pas autorisé. Les sous-ensembles de polices peuvent également enfreindre les termes de la licence.

### Exemples

Montre comment définir une logique personnalisée pour l’exportation des polices lors de l’enregistrement au format HTML.

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
/// Imprime les informations sur les polices exportées et les enregistre dans le même dossier système local que leur sortie .html.
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

        // Il existe deux manières de sauvegarder une police exportée.
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

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


