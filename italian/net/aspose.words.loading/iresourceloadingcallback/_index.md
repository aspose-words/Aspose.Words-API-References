---
title: IResourceLoadingCallback Interface
linktitle: IResourceLoadingCallback
articleTitle: IResourceLoadingCallback
second_title: Aspose.Words per .NET
description: Aspose.Words.Loading.IResourceLoadingCallback interfaccia. Implementa questa interfaccia se desideri controllare il modo in cui Aspose.Words carica le risorse esterne quando importi un documento e inserisci immagini utilizzandoDocumentBuilder  in C#.
type: docs
weight: 3640
url: /it/net/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface

Implementa questa interfaccia se desideri controllare il modo in cui Aspose.Words carica le risorse esterne quando importi un documento e inserisci immagini utilizzando[`DocumentBuilder`](../../aspose.words/documentbuilder/) .

```csharp
public interface IResourceLoadingCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ResourceLoading](../../aspose.words.loading/iresourceloadingcallback/resourceloading/)(*[ResourceLoadingArgs](../resourceloadingargs/)*) | Chiamato quando Aspose.Words carica una risorsa esterna. |

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

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
