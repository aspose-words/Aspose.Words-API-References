---
title: IResourceLoadingCallback.ResourceLoading
linktitle: ResourceLoading
articleTitle: ResourceLoading
second_title: Aspose.Words per .NET
description: IResourceLoadingCallback ResourceLoading metodo. Chiamato quando Aspose.Words carica una risorsa esterna in C#.
type: docs
weight: 10
url: /it/net/aspose.words.loading/iresourceloadingcallback/resourceloading/
---
## IResourceLoadingCallback.ResourceLoading method

Chiamato quando Aspose.Words carica una risorsa esterna.

```csharp
public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
```

## Esempi

Mostra come personalizzare il processo di caricamento delle risorse esterne in un documento.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Le immagini solitamente vengono inserite utilizzando un URI o un array di byte.
    // Ogni istanza di caricamento di una risorsa chiamerà il metodo ResourceLoading del nostro callback.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Ci consente di caricare immagini in un documento utilizzando abbreviazioni predefinite, anziché URI.
/// Ciò separerà la logica di caricamento dell'immagine dal resto della costruzione del documento.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Se questo callback incontra una delle scorciatoie dell'immagine durante il caricamento di un'immagine,
        // applicherà una logica univoca per ogni abbreviazione definita invece di trattarla come un URI.
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

### Guarda anche

* enum [ResourceLoadingAction](../../resourceloadingaction/)
* class [ResourceLoadingArgs](../../resourceloadingargs/)
* interface [IResourceLoadingCallback](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
