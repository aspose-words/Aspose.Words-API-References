---
title: DocumentBase.ResourceLoadingCallback
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBase propriété. Permet de contrôler la manière dont les ressources externes sont chargées.
type: docs
weight: 70
url: /fr/net/aspose.words/documentbase/resourceloadingcallback/
---
## DocumentBase.ResourceLoadingCallback property

Permet de contrôler la manière dont les ressources externes sont chargées.

```csharp
public IResourceLoadingCallback ResourceLoadingCallback { get; set; }
```

### Exemples

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

* interface [IResourceLoadingCallback](../../../aspose.words.loading/iresourceloadingcallback/)
* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../documentbase/)
* Assemblée [Aspose.Words](../../../)


