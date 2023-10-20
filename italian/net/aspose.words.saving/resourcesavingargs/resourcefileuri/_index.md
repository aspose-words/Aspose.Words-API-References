---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words per .NET
description: ResourceSavingArgs ResourceFileUri proprietà. Ottiene o imposta lURI Uniform Resource Identifier utilizzato per fare riferimento al file di risorse dal documento in C#.
type: docs
weight: 40
url: /it/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Ottiene o imposta l'URI (Uniform Resource Identifier) utilizzato per fare riferimento al file di risorse dal documento.

```csharp
public string ResourceFileUri { get; set; }
```

## Osservazioni

Questa proprietà consente di modificare gli URI dei file di risorse esportati in documenti HTML o SVG a pagina fissa.

Aspose.Words genera automaticamente un URI per ogni file di risorse durante l'esportazione nel formato HTML o SVG a pagina fissa. Gli URI generati fanno riferimento ai file di risorse salvati da Aspose.Words. Tuttavia, gli URI possono essere errati se i file di risorse devono essere spostati in un'altra posizione o se i file di risorse vengono salvati negli stream. Questa proprietà consente di correggere gli URI in questi casi.

Quando l'evento viene generato, questa proprietà contiene l'URI che è stato generato da Aspose.Words. È possibile modificare il valore di questa proprietà per fornire un URI personalizzato per il file di risorse.

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
    /// Chiamato quando Aspose.Words salva una risorsa esterna su una pagina HTML o SVG fissa.
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
