---
title: ResourceSavingArgs.KeepResourceStreamOpen
linktitle: KeepResourceStreamOpen
articleTitle: KeepResourceStreamOpen
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété KeepResourceStreamOpen dans ResourceSavingArgs améliore Aspose.Words en gérant l'efficacité du flux lors de l'économie de ressources.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/resourcesavingargs/keepresourcestreamopen/
---
## ResourceSavingArgs.KeepResourceStreamOpen property

Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après avoir enregistré une ressource.

```csharp
public bool KeepResourceStreamOpen { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` et Aspose.Words fermera le flux que vous avez fourni dans le[`ResourceStream`](../resourcestream/) propriété après avoir écrit une ressource dedans. Spécifier`vrai` pour garder le ruisseau ouvert.

## Exemples

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

* class [ResourceSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
