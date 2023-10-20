---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: Aspose.Words pour .NET
description: Aspose.Words.Loading.ResourceLoadingArgs classe. Fournit des données pour leResourceLoading méthode en C#.
type: docs
weight: 3690
url: /fr/net/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class

Fournit des données pour le[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) méthode.

```csharp
public class ResourceLoadingArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | URI d'origine de la ressource tel que spécifié dans le document importé. |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | Type de ressource. |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | URI de la ressource utilisée pour le téléchargement si[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) renvoieDefault. |

## Méthodes

| Nom | La description |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | Définit les données fournies par l'utilisateur de la ressource qui est utilisée si[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) renvoieUserProvided . |

## Exemples

Montre comment personnaliser le processus de chargement de ressources externes dans un document.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Les images sont généralement insérées à l'aide d'un URI ou d'un tableau d'octets.
    // Chaque instance d'un chargement de ressource appellera la méthode ResourceLoading de notre rappel.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Nous permet de charger des images dans un document à l'aide de raccourcis prédéfinis, par opposition aux URI.
/// Cela séparera la logique de chargement de l'image du reste de la construction du document.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Si ce rappel rencontre l'un des raccourcis d'image lors du chargement d'une image,
        // il appliquera une logique unique pour chaque raccourci défini au lieu de le traiter comme un URI.
        if (args.ResourceType == ResourceType.Image)
            switch (args.OriginalUri)
            {
                case "Google logo":
                    using (WebClient webClient = new WebClient())
                    {
                        args.SetData(webClient.DownloadData("http://www.google.com/images/logos/ps_logo2.png"));
                    }

                    return ResourceLoadingAction.UserProvided;

                case "Aspose logo":
                    args.SetData(File.ReadAllBytes(ImageDir + "Logo.jpg"));

                    return ResourceLoadingAction.UserProvided;

                case "Watermark":
                    args.SetData(File.ReadAllBytes(ImageDir + "Transparent background logo.png"));

                    return ResourceLoadingAction.UserProvided;
            }

        return ResourceLoadingAction.Default;
    }
}
```

### Voir également

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
