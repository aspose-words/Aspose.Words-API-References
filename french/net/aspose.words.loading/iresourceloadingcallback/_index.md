---
title: IResourceLoadingCallback Interface
linktitle: IResourceLoadingCallback
articleTitle: IResourceLoadingCallback
second_title: Aspose.Words pour .NET
description: Contrôlez le chargement des ressources externes dans Aspose.Words grâce à l'interface IResourceLoadingCallback. Améliorez l'importation de documents et l'insertion d'images en toute fluidité.
type: docs
weight: 4090
url: /fr/net/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface

Implémentez cette interface si vous souhaitez contrôler la manière dont Aspose.Words charge les ressources externes lors de l'importation d'un document et de l'insertion d'images à l'aide de[`DocumentBuilder`](../../aspose.words/documentbuilder/) .

```csharp
public interface IResourceLoadingCallback
```

## Méthodes

| Nom | La description |
| --- | --- |
| [ResourceLoading](../../aspose.words.loading/iresourceloadingcallback/resourceloading/)(*[ResourceLoadingArgs](../resourceloadingargs/)*) | Appelé lorsque Aspose.Words charge une ressource externe. |

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
/// Nous permet de charger des images dans un document en utilisant des raccourcis prédéfinis, par opposition aux URI.
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
