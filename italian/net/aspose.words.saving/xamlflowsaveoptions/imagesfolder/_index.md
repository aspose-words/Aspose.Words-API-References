---
title: XamlFlowSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ImagesFolder di XamlFlowSaveOptions consente di specificare facilmente una cartella in cui salvare le immagini durante l'esportazione di documenti in formato XAML.
type: docs
weight: 30
url: /it/net/aspose.words.saving/xamlflowsaveoptions/imagesfolder/
---
## XamlFlowSaveOptions.ImagesFolder property

Specifica la cartella fisica in cui vengono salvate le immagini durante l'esportazione di un documento in formato XAML. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolder { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) nel formato XAML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi.`ImagesFolder` consente di specificare dove verranno salvate le immagini e[`ImagesFolderAlias`](../imagesfolderalias/) consente di specificare come verranno costruiti gli URI delle immagini.

Se si salva un documento in un file e si specifica un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Utilizzare`ImagesFolder` per ignorare questo comportamento.

Se si salva un documento in un flusso, Aspose.Words non ha una cartella in cui salvare le immagini, , ma deve comunque salvarle da qualche parte. In questo caso, è necessario specificare una cartella accessibile nel`ImagesFolder` proprietà o fornire flussi personalizzati tramite [`ImageSavingCallback`](../imagesavingcallback/) gestore degli eventi.

## Esempi

Mostra come stampare i nomi dei file delle immagini collegate create durante la conversione di un documento in formato flow-form .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Creiamo un oggetto "XamlFlowSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui salviamo il documento nel formato di salvataggio XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Utilizzare la proprietà "ImagesFolder" per assegnare una cartella nel file system locale in cui
    // Aspose.Words salverà tutte le immagini collegate del documento.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Utilizzare la proprietà "ImagesFolderAlias" per utilizzare questa cartella
    // quando si costruiscono gli URI delle immagini invece del nome della cartella delle immagini.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Una cartella specificata da "ImagesFolderAlias" dovrà contenere le risorse al posto di "ImagesFolder".
    // Dobbiamo assicurarci che la cartella esista prima che i flussi del callback possano inserirvi le proprie risorse.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Conta e stampa i nomi dei file delle immagini mentre il documento padre viene convertito in formato flow-form .xaml.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // Se specificassimo un alias di cartella immagini, avremmo anche bisogno
        // per reindirizzare ogni flusso in modo che inserisca la sua immagine nella cartella alias.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Guarda anche

* class [XamlFlowSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
