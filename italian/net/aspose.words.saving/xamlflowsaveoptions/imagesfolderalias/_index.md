---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImagesFolderAlias di XamlFlowSaveOptions per personalizzare i percorsi URI delle immagini nei documenti XAML. Migliora i tuoi progetti con facilità!
type: docs
weight: 40
url: /it/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI delle immagini scritti in un documento XAML. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) nel formato XAML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi.[`ImagesFolder`](../imagesfolder/) consente di specificare dove verranno salvate le immagini e`ImagesFolderAlias` consente di specificare come verranno costruiti gli URI delle immagini.

Se`ImagesFolderAlias` non è una stringa vuota, allora l'URI dell'immagine scritto in XAML saràImagesFolderAlias + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias` è una stringa vuota, quindi l'URI dell'immagine scritto in XAML saràImagesFolder + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias` è impostato su '.' (punto), il nome del file immagine verrà scritto in XAML senza percorso, indipendentemente dalle altre opzioni.

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
