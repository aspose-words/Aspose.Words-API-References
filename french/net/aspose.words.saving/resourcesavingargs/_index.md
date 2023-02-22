---
title: Class ResourceSavingArgs
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.ResourceSavingArgs classe. Fournit des données pour leResourceSaving événement.
type: docs
weight: 5280
url: /fr/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Fournit des données pour le[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) événement.

```csharp
public class ResourceSavingArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Obtient l'objet document en cours d'enregistrement. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après avoir enregistré une ressource. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Obtient ou définit le nom du fichier (sans chemin) dans lequel la ressource sera enregistrée. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Obtient ou définit l'URI (Uniform Resource Identifier) utilisé pour référencer le fichier de ressources à partir du document. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Permet de spécifier le flux dans lequel la ressource sera enregistrée. |

### Remarques

Par défaut, lorsque Aspose.Words enregistre un document en HTML ou SVG à page fixe, il enregistre chaque ressource dans un fichier séparé. Aspose.Words utilise le nom de fichier du document et un numéro unique pour générer un nom de fichier unique pour chaque ressource trouvée dans le document.

`ResourceSavingArgs` permet de redéfinir la façon dont les noms de fichiers de ressources sont générés ou de contourner complètement l'enregistrement des ressources dans des fichiers en fournissant vos propres objets de flux.

Pour appliquer votre propre logique pour générer des noms de fichiers de ressources, utilisez le [`ResourceFileName`](./resourcefilename/) propriété.

Pour enregistrer les ressources dans des flux au lieu de fichiers, utilisez la[`ResourceStream`](./resourcestream/) propriété.

### Exemples

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document au format HTML.

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
    /// Appelé quand Aspose.Words enregistre une ressource externe dans une page fixe HTML ou SVG.
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


