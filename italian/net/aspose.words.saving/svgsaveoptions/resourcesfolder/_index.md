---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words per .NET
description: Scopri come impostare ResourcesFolder in SvgSaveOptions per un'archiviazione efficiente delle immagini durante l'esportazione di documenti in formato SVG. Ottimizza il tuo flusso di lavoro oggi stesso!
type: docs
weight: 80
url: /it/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Specifica la cartella fisica in cui vengono salvate le risorse (immagini) durante l'esportazione di un documento in formato Svg. Il valore predefinito è`null` .

```csharp
public string ResourcesFolder { get; set; }
```

## Osservazioni

Ha effetto solo se[`ExportEmbeddedImages`](../exportembeddedimages/) la proprietà è`falso`.

Quando salvi un[`Document`](../../../aspose.words/document/) nel formato SVG, Aspose.Words deve salvare tutte le immagini x000d incorporate nel documento come file autonomi.`ResourcesFolder` consente di specificare dove verranno salvate le immagini e[`ResourcesFolderAlias`](../resourcesfolderalias/) consente di specificare come verranno costruiti gli URI delle immagini.

Se si salva un documento in un file e si fornisce un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Utilizzare`ResourcesFolder` per ignorare questo comportamento.

Se si salva un documento in un flusso, Aspose.Words non ha una cartella in cui salvare le immagini, , ma deve comunque salvarle da qualche parte. In questo caso, è necessario specificare una cartella accessibile nel`ResourcesFolder` proprietà

## Esempi

Mostra come manipolare e stampare gli URI delle risorse collegate create durante la conversione di un documento in .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// Conta e stampa gli URI delle risorse contenute in quando vengono convertiti in .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### Guarda anche

* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
