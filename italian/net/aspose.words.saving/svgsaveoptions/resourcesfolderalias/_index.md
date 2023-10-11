---
title: SvgSaveOptions.ResourcesFolderAlias
second_title: Aspose.Words per .NET API Reference
description: SvgSaveOptions proprietà. Specifica il nome della cartella utilizzata per costruire gli URI di immagine scritti in un documento SVG. Limpostazione predefinita ènullo .
type: docs
weight: 60
url: /it/net/aspose.words.saving/svgsaveoptions/resourcesfolderalias/
---
## SvgSaveOptions.ResourcesFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI di immagine scritti in un documento SVG. L'impostazione predefinita è`nullo` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

### Osservazioni

Quando salvi un file[`Document`](../../../aspose.words/document/) nel formato SVG, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi.[`ResourcesFolder`](../resourcesfolder/) ti consente di specificare dove verranno salvate le immagini e`ResourcesFolderAlias` consente di specificare come verranno costruiti gli URI dell'immagine.

### Esempi

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
* spazio dei nomi [Aspose.Words.Saving](../../svgsaveoptions/)
* assemblea [Aspose.Words](../../../)


