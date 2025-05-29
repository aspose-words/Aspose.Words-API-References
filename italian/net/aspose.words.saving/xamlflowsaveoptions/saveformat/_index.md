---
title: XamlFlowSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà SaveFormat di XamlFlowSaveOptions per salvare facilmente i tuoi documenti in formato XamlFlow. Ottimizza il tuo flusso di lavoro con questa funzionalità essenziale!
type: docs
weight: 60
url: /it/net/aspose.words.saving/xamlflowsaveoptions/saveformat/
---
## XamlFlowSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloXamlFlow .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XamlFlowSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
