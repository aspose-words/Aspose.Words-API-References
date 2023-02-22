---
title: SvgSaveOptions.ResourceSavingCallback
second_title: Aspose.Words per .NET API Reference
description: SvgSaveOptions proprietà. Consente di controllare come vengono salvate le risorse immagini quando un documento viene esportato in formato SVG.
type: docs
weight: 40
url: /it/net/aspose.words.saving/svgsaveoptions/resourcesavingcallback/
---
## SvgSaveOptions.ResourceSavingCallback property

Consente di controllare come vengono salvate le risorse (immagini) quando un documento viene esportato in formato SVG.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

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
/// Conta e stampa gli URI delle risorse contenute in quando vengono convertite in .svg.
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

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../svgsaveoptions/)
* assemblea [Aspose.Words](../../../)


