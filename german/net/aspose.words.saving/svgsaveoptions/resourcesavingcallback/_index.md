---
title: ResourceSavingCallback
second_title: Aspose.Words für .NET-API-Referenz
description: Ermöglicht die Steuerung wie Ressourcen Bilder gespeichert werden wenn ein Dokument in das SVG-Format exportiert wird.
type: docs
weight: 40
url: /de/net/aspose.words.saving/svgsaveoptions/resourcesavingcallback/
---
## SvgSaveOptions.ResourceSavingCallback property

Ermöglicht die Steuerung, wie Ressourcen (Bilder) gespeichert werden, wenn ein Dokument in das SVG-Format exportiert wird.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

### Beispiele

Zeigt, wie die URIs verknüpfter Ressourcen bearbeitet und gedruckt werden, die beim Konvertieren eines Dokuments in .svg erstellt wurden.

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
/// Zählt und druckt URIs von Ressourcen, die in enthalten sind, während sie in .svg konvertiert werden.
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

### Siehe auch

* interface [IResourceSavingCallback](../../iresourcesavingcallback)
* class [SvgSaveOptions](../../svgsaveoptions)
* namensraum [Aspose.Words.Saving](../../svgsaveoptions)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->