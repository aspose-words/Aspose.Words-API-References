---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.ResourceSavingArgs, che migliora l'elaborazione dei documenti fornendo dati essenziali per l'evento ResourceSaving.
type: docs
weight: 6360
url: /it/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Fornisce dati per il[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) evento.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class ResourceSavingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Ottiene l'oggetto documento che è attualmente in fase di salvataggio. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Specifica se Aspose.Words deve mantenere aperto il flusso o chiuderlo dopo aver salvato una risorsa. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Ottiene o imposta il nome del file (senza percorso) in cui verrà salvata la risorsa. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Ottiene o imposta l'URI (Uniform Resource Identifier) utilizzato per fare riferimento al file di risorse dal documento. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Consente di specificare il flusso in cui verrà salvata la risorsa. |

## Osservazioni

Per impostazione predefinita, quando Aspose.Words salva un documento in formato HTML o SVG a pagina fissa, salva ogni risorsa in un file separato . Aspose.Words utilizza il nome del file del documento e un numero univoco per generare un file name univoco per ogni risorsa presente nel documento.

`ResourceSavingArgs` consente di ridefinire il modo in cui vengono generati i nomi dei file di risorse o di aggirare completamente il salvataggio delle risorse nei file fornendo i propri oggetti stream.

Per applicare la tua logica per generare nomi di file di risorse usa [`ResourceFileName`](./resourcefilename/) proprietà.

Per salvare le risorse in flussi anziché in file, utilizzare[`ResourceStream`](./resourcestream/) proprietà.

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
