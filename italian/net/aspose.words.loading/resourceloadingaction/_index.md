---
title: ResourceLoadingAction Enum
linktitle: ResourceLoadingAction
articleTitle: ResourceLoadingAction
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.ResourceLoadingAction per modalità di caricamento risorse efficienti. Migliora l'elaborazione dei tuoi documenti con prestazioni ottimizzate!
type: docs
weight: 4140
url: /it/net/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enumeration

Specifica la modalità di caricamento delle risorse.

Per saperne di più, visita il[Specificare le opzioni di carico](https://docs.aspose.com/words/net/specify-load-options/) articolo di documentazione.

```csharp
public enum ResourceLoadingAction
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Aspose.Words caricherà questa risorsa come di consueto. |
| Skip | `1` | Aspose.Words salterà il caricamento di questa risorsa. Per un'immagine verrà memorizzato solo il collegamento senza dati, il foglio di stile CSS verrà ignorato per il formato HTML. |
| UserProvided | `2` | Aspose.Words utilizzerà l'array di byte fornito dall'utente in[`SetData`](../resourceloadingargs/setdata/) come dati di risorse. |

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
