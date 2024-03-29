---
title: SvgSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words pour .NET
description: SvgSaveOptions ExportEmbeddedImages propriété. Spécifié si les images doivent être intégrées dans le document SVG en base64. Remarque  la définition de cet indicateur peut augmenter considérablement la taille du fichier SVG de sortie en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

Spécifié si les images doivent être intégrées dans le document SVG en base64. Remarque : la définition de cet indicateur peut augmenter considérablement la taille du fichier SVG de sortie.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

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
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
