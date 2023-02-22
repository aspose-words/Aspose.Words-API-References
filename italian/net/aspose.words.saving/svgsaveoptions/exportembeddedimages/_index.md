---
title: SvgSaveOptions.ExportEmbeddedImages
second_title: Aspose.Words per .NET API Reference
description: SvgSaveOptions proprietà. Specifica se le immagini devono essere incorporate nel documento SVG come base64. Nota limpostazione di questo flag può aumentare significativamente le dimensioni del file SVG di output.
type: docs
weight: 20
url: /it/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

Specifica se le immagini devono essere incorporate nel documento SVG come base64. Nota l'impostazione di questo flag può aumentare significativamente le dimensioni del file SVG di output.

```csharp
public bool ExportEmbeddedImages { get; set; }
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

* class [SvgSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../svgsaveoptions/)
* assemblea [Aspose.Words](../../../)


