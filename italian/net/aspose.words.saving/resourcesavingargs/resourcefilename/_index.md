---
title: ResourceSavingArgs.ResourceFileName
linktitle: ResourceFileName
articleTitle: ResourceFileName
second_title: Aspose.Words per .NET
description: Gestisci le tue risorse in modo efficiente con ResourceSavingArgs. Imposta o recupera facilmente il nome del file per salvare le risorse, senza la necessità di percorsi.
type: docs
weight: 30
url: /it/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

Ottiene o imposta il nome del file (senza percorso) in cui verrà salvata la risorsa.

```csharp
public string ResourceFileName { get; set; }
```

## Osservazioni

Questa proprietà consente di ridefinire il modo in cui vengono generati i nomi dei file di risorse durante l'esportazione in HTML o SVG di pagina fissa.

Quando l'evento viene attivato, questa proprietà contiene il nome del file generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare la risorsa in un file diverso. Si noti che i nomi dei file devono essere univoci.

Aspose.Words genera automaticamente un nome file univoco per ogni risorsa quando si esporta in formato HTML o SVG a pagina fissa. Il modo in cui viene generato il nome del file della risorsa varia a seconda che il documento venga salvato in un file o in un flusso.

Quando si salva un documento in un file, il nome del file di risorse generato appare come &lt;nome file base documento&gt;.&lt;numero immagine&gt;.&lt;estensione&gt;.

Quando si salva un documento in un flusso, il nome del file di risorse generato appare come Aspose.Words.&lt;guid documento&gt;.&lt;numero immagine&gt;.&lt;estensione&gt;.

`ResourceFileName` deve contenere solo il nome del file senza il percorso. Aspose.Words determina il percorso per il salvataggio e il valore del`fonte` attributo per scrivere in una pagina HTML o SVG fissa utilizzando il nome del file del documento,[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) o[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) E[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) o[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) proprietà.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

## Esempi

Mostra come utilizzare un callback per tenere traccia delle risorse esterne create durante la conversione di un documento in HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// Chiamato quando Aspose.Words salva una risorsa esterna in una pagina HTML o SVG fissa.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

### Guarda anche

* class [ResourceSavingArgs](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
