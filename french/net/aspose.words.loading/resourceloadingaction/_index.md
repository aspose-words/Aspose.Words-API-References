---
title: ResourceLoadingAction Enum
linktitle: ResourceLoadingAction
articleTitle: ResourceLoadingAction
second_title: Aspose.Words pour .NET
description: Aspose.Words.Loading.ResourceLoadingAction énumération. Spécifie le mode de chargement des ressources en C#.
type: docs
weight: 3680
url: /fr/net/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enumeration

Spécifie le mode de chargement des ressources.

Pour en savoir plus, visitez le[Spécifier les options de chargement](https://docs.aspose.com/words/net/specify-load-options/) article documentaire.

```csharp
public enum ResourceLoadingAction
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Default | `0` | Aspose.Words chargera cette ressource comme d'habitude. |
| Skip | `1` | Aspose.Words ignorera le chargement de cette ressource. Seul le lien sans données sera stocké pour une image, la feuille de style CSS sera ignorée pour le format HTML. |
| UserProvided | `2` | Aspose.Words utilisera le tableau d'octets fourni par l'utilisateur dans[`SetData`](../resourceloadingargs/setdata/) comme données de ressources. |

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
