---
title: ResourceType Enum
linktitle: ResourceType
articleTitle: ResourceType
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.ResourceType per una gestione efficiente delle risorse. Migliora l'elaborazione dei tuoi documenti con opzioni di caricamento versatili.
type: docs
weight: 4160
url: /it/net/aspose.words.loading/resourcetype/
---
## ResourceType enumeration

Tipo di risorsa caricata.

```csharp
public enum ResourceType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Image | `0` | Immagine. |
| Font | `1` | Carattere. |
| CssStyleSheet | `2` | Foglio di stile CSS. |
| Document | `3` | Documento. |

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

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
