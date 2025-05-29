---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.ResourceSavingArgs, qui améliore le traitement de vos documents en fournissant des données essentielles pour l'événement ResourceSaving.
type: docs
weight: 6360
url: /fr/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Fournit des données pour le[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) événement.

Pour en savoir plus, visitez le[Enregistrer un document](https://docs.aspose.com/words/net/save-a-document/) article de documentation.

```csharp
public class ResourceSavingArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Obtient l'objet document en cours d'enregistrement. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après avoir enregistré une ressource. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Obtient ou définit le nom du fichier (sans chemin) dans lequel la ressource sera enregistrée. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Obtient ou définit l'identifiant de ressource uniforme (URI) utilisé pour référencer le fichier de ressources à partir du document. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Permet de spécifier le flux dans lequel la ressource sera enregistrée. |

## Remarques

Par défaut, lorsqu'Aspose.Words enregistre un document au format HTML ou SVG, il enregistre chaque ressource dans un fichier distinct. Aspose.Words utilise le nom de fichier du document et un numéro unique pour générer un nom de fichier unique pour chaque ressource présente dans le document.

`ResourceSavingArgs` permet de redéfinir la manière dont les noms de fichiers de ressources sont générés ou de contourner complètement l'enregistrement des ressources dans les fichiers en fournissant vos propres objets de flux.

Pour appliquer votre propre logique de génération de noms de fichiers de ressources, utilisez [`ResourceFileName`](./resourcefilename/) propriété.

Pour enregistrer des ressources dans des flux plutôt que dans des fichiers, utilisez le[`ResourceStream`](./resourcestream/) propriété.

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

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
