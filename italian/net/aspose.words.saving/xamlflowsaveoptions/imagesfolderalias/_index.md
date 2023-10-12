---
title: XamlFlowSaveOptions.ImagesFolderAlias
second_title: Aspose.Words per .NET API Reference
description: XamlFlowSaveOptions proprietà. Specifica il nome della cartella utilizzata per costruire URI di immagine scritti in un documento XAML. Il valore predefinito è una stringa vuota.
type: docs
weight: 40
url: /it/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

Specifica il nome della cartella utilizzata per costruire URI di immagine scritti in un documento XAML. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolderAlias { get; set; }
```

### Osservazioni

Quando salvi un file[`Document`](../../../aspose.words/document/) nel formato XAML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi.[`ImagesFolder`](../imagesfolder/) ti consente di specificare dove verranno salvate le immagini e`ImagesFolderAlias` consente di specificare come verranno costruiti gli URI dell'immagine.

Se`ImagesFolderAlias` non è una stringa vuota, lo sarà l'URI dell'immagine scritto in XAMLImagesFolderAlias + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias`è una stringa vuota, l'URI dell'immagine scritto in XAML saràCartella Immagini + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias` è impostato per '.' (punto), il nome del file immagine verrà scritto in XAML senza percorso indipendentemente dalle altre opzioni.

### Esempi

Mostra come stampare i nomi file delle immagini collegate create durante la conversione di un documento in formato flusso .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Crea un oggetto "XamlFlowSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui salviamo il documento nel formato di salvataggio XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Utilizzare la proprietà "ImagesFolder" per assegnare una cartella nel file system locale in cui
    // Aspose.Words salverà tutte le immagini collegate del documento.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Utilizzare la proprietà "ImagesFolderAlias" per utilizzare questa cartella
    // quando si costruiscono URI di immagine invece del nome della cartella delle immagini.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Una cartella specificata da "ImagesFolderAlias" dovrà contenere le risorse invece di "ImagesFolder".
    // Dobbiamo garantire che la cartella esista prima che i flussi di callback possano inserirvi le proprie risorse.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Conta e stampa i nomi file delle immagini mentre il documento principale viene convertito in formato flusso .xaml.
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

        // Se specificassimo un alias di cartella immagine, avremmo anche bisogno
        // per reindirizzare ciascun flusso per inserire la relativa immagine nella cartella alias.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Guarda anche

* class [XamlFlowSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* assemblea [Aspose.Words](../../../)


