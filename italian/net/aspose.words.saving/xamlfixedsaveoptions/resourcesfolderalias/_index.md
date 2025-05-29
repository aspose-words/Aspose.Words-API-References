---
title: XamlFixedSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ResourcesFolderAlias in XamlFixedSaveOptions migliora la gestione degli URI delle immagini nei documenti Xaml. Ottimizza subito i tuoi layout di pagina fissi!
type: docs
weight: 40
url: /it/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/
---
## XamlFixedSaveOptions.ResourcesFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI delle immagini scritti in un documento Xaml a pagina fissa. Il valore predefinito è`null` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) nel formato Xaml a pagina fissa, Aspose.Words deve salvare tutte le immagini x000d incorporate nel documento come file autonomi.[`ResourcesFolder`](../resourcesfolder/) consente di specificare dove verranno salvate le immagini e`ResourcesFolderAlias` consente di specificare come verranno costruiti gli URI delle immagini.

## Esempi

Mostra come stampare gli URI delle risorse collegate create durante la conversione di un documento in un file .xaml in formato fisso.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Creiamo un oggetto "XamlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui salviamo il documento nel formato di salvataggio XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilizzare la proprietà "ResourcesFolder" per assegnare una cartella nel file system locale in cui
    // Aspose.Words salverà tutte le risorse collegate del documento, come immagini e font.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Utilizzare la proprietà "ResourcesFolderAlias" per utilizzare questa cartella
    // quando si costruiscono gli URI delle immagini invece del nome della cartella delle risorse.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Una cartella specificata da "ResourcesFolderAlias" dovrà contenere le risorse anziché "ResourcesFolder".
    // Dobbiamo assicurarci che la cartella esista prima che i flussi del callback possano inserirvi le proprie risorse.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Conta e stampa gli URI delle risorse create durante la conversione in .xaml fisso.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // Se specificassimo un alias della cartella delle risorse, avremmo anche bisogno
        // per reindirizzare ogni flusso in modo che inserisca la sua risorsa nella cartella alias.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Guarda anche

* class [XamlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
