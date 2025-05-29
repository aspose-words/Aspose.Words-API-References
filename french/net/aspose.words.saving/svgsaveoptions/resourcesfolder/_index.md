---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words pour .NET
description: Découvrez comment configurer le dossier ResourcesFolder dans SvgSaveOptions pour un stockage efficace des images lors de l'exportation de documents au format SVG. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 80
url: /fr/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Spécifie le dossier physique dans lequel les ressources (images) sont enregistrées lors de l'exportation d'un document au format Svg. La valeur par défaut est`nul` .

```csharp
public string ResourcesFolder { get; set; }
```

## Remarques

N'a d'effet que si[`ExportEmbeddedImages`](../exportembeddedimages/) la propriété est`FAUX`.

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format SVG, Aspose.Words doit enregistrer toutes les images intégrées dans le document en tant que fichiers autonomes.`ResourcesFolder` vous permet de spécifier où les images seront enregistrées et[`ResourcesFolderAlias`](../resourcesfolderalias/) permet de spécifier comment les URI des images seront construits.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier où le fichier du document est enregistré.`ResourcesFolder` pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words ne dispose pas de dossier pour enregistrer les images, mais doit tout de même les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible dans le fichier`ResourcesFolder` propriété

## Exemples

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
/// Compte et imprime les URI des ressources contenues par lorsqu'elles sont converties en .svg.
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
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
