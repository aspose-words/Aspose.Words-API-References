---
title: DocumentBase.ResourceLoadingCallback
linktitle: ResourceLoadingCallback
articleTitle: ResourceLoadingCallback
second_title: Aspose.Words per .NET
description: Ottimizza DocumentBase con la proprietà ResourceLoadingCallback per un controllo efficiente sul caricamento di risorse esterne. Migliora le prestazioni oggi stesso!
type: docs
weight: 80
url: /it/net/aspose.words/documentbase/resourceloadingcallback/
---
## DocumentBase.ResourceLoadingCallback property

Consente di controllare come vengono caricate le risorse esterne.

```csharp
public IResourceLoadingCallback ResourceLoadingCallback { get; set; }
```

## Esempi

Mostra come personalizzare il processo di caricamento di risorse esterne in un documento.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Le immagini vengono solitamente inserite tramite un URI o un array di byte.
    // Ogni istanza di caricamento di una risorsa chiamerà il metodo ResourceLoading del nostro callback.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Consente di caricare immagini in un documento utilizzando abbreviazioni predefinite, anziché URI.
/// In questo modo la logica di caricamento delle immagini verrà separata dal resto della costruzione del documento.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Se questo callback incontra una delle abbreviazioni dell'immagine durante il caricamento di un'immagine,
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

* interface [IResourceLoadingCallback](../../../aspose.words.loading/iresourceloadingcallback/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
