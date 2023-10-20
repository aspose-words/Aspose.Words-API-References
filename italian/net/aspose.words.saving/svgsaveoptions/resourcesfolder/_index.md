---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words per .NET
description: SvgSaveOptions ResourcesFolder proprietà. Specifica la cartella fisica in cui vengono salvate le risorse immagini durante lesportazione di un documento in formato Svg. Limpostazione predefinita ènullo  in C#.
type: docs
weight: 50
url: /it/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Specifica la cartella fisica in cui vengono salvate le risorse (immagini) durante l'esportazione di un documento in formato Svg. L'impostazione predefinita è`nullo` .

```csharp
public string ResourcesFolder { get; set; }
```

## Osservazioni

Ha effetto solo se[`ExportEmbeddedImages`](../exportembeddedimages/) la proprietà è`falso`.

Quando salvi un file[`Document`](../../../aspose.words/document/) nel formato SVG, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi.`ResourcesFolder` ti consente di specificare dove verranno salvate le immagini e[`ResourcesFolderAlias`](../resourcesfolderalias/) consente di specificare come verranno costruiti gli URI dell'immagine.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Utilizzo`ResourcesFolder` per sovrascrivere questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non ha una cartella in cui salvare le immagini, ma deve comunque salvare le immagini da qualche parte. In questo caso, devi specificare una cartella accessibile nel file`ResourcesFolder` proprietà

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
/// Conta e stampa gli URI delle risorse contenute da quando vengono convertiti in .svg.
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
