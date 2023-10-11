---
title: SvgSaveOptions.ResourcesFolderAlias
second_title: Référence de l'API Aspose.Words pour .NET
description: SvgSaveOptions propriété. Spécifie le nom du dossier utilisé pour construire les URI dimage écrits dans un document SVG. La valeur par défaut estnul .
type: docs
weight: 60
url: /fr/net/aspose.words.saving/svgsaveoptions/resourcesfolderalias/
---
## SvgSaveOptions.ResourcesFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI d'image écrits dans un document SVG. La valeur par défaut est`nul` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

### Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format SVG, Aspose.Words doit enregistrer toutes les images intégrées dans le document en tant que fichiers autonomes.[`ResourcesFolder`](../resourcesfolder/) permet de préciser où les images seront enregistrées et`ResourcesFolderAlias` permet de spécifier comment les URI des images seront construites.

### Exemples

Montre comment manipuler et imprimer les URI des ressources liées créées lors de la conversion d'un document en .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// Compte et imprime les URI des ressources contenues par au fur et à mesure de leur conversion en .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### Voir également

* class [SvgSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../svgsaveoptions/)
* Assemblée [Aspose.Words](../../../)


