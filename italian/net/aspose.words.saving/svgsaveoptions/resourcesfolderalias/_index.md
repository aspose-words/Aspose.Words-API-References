---
title: SvgSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: Aspose.Words per .NET
description: Scopri la proprietà ResourcesFolderAlias di SvgSaveOptions per personalizzare gli URI delle immagini nei documenti SVG. Migliora il tuo output SVG con una denominazione flessibile delle cartelle!
type: docs
weight: 90
url: /it/net/aspose.words.saving/svgsaveoptions/resourcesfolderalias/
---
## SvgSaveOptions.ResourcesFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI delle immagini scritti in un documento SVG. Il valore predefinito è`null` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) nel formato SVG, Aspose.Words deve salvare tutte le immagini x000d incorporate nel documento come file autonomi.[`ResourcesFolder`](../resourcesfolder/) consente di specificare dove verranno salvate le immagini e`ResourcesFolderAlias` consente di specificare come verranno costruiti gli URI delle immagini.

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
