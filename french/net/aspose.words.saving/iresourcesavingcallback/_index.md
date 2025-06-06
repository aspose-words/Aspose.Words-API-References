---
title: IResourceSavingCallback Interface
linktitle: IResourceSavingCallback
articleTitle: IResourceSavingCallback
second_title: Aspose.Words pour .NET
description: Contrôlez les économies de ressources d'Aspose.Words grâce à l'interface IResourceSavingCallback. Gérez les images, les polices et le CSS pour des documents HTML ou SVG optimisés.
type: docs
weight: 5940
url: /fr/net/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface

Implémentez cette interface si vous souhaitez contrôler la manière dont Aspose.Words enregistre les ressources externes (images, polices et CSS) lors de l'enregistrement d'un document au format HTML ou SVG à page fixe.

```csharp
public interface IResourceSavingCallback
```

## Méthodes

| Nom | La description |
| --- | --- |
| [ResourceSaving](../../aspose.words.saving/iresourcesavingcallback/resourcesaving/)(*[ResourceSavingArgs](../resourcesavingargs/)*) | Appelé lorsque Aspose.Words enregistre une ressource externe dans des formats HTML ou SVG de page fixe. |

## Exemples

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document en HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// Appelé lorsque Aspose.Words enregistre une ressource externe dans une page fixe HTML ou SVG.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

Montre comment utiliser un rappel pour imprimer les URI des ressources externes créées lors de la conversion d'un document en HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // Un dossier spécifié par ResourcesFolderAlias contiendra les ressources au lieu de ResourcesFolder.
    // Nous devons nous assurer que le dossier existe avant que les flux puissent y placer leurs ressources.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Compte et imprime les URI des ressources contenues par lorsqu'elles sont converties en HTML fixe.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Si nous définissons un alias de dossier dans l'objet SaveOptions, nous pourrons l'imprimer à partir d'ici.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Par défaut, 'ResourceFileUri' utilise le dossier système pour les polices.
                // Pour éviter les problèmes sur d'autres plateformes, vous devez spécifier explicitement le chemin des polices.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Si nous avons spécifié un dossier dans la propriété "ResourcesFolderAlias",
        // nous devrons également rediriger chaque flux pour placer sa ressource dans ce dossier.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
