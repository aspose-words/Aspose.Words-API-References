---
title: SvgSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveFormat-Eigenschaft von SvgSaveOptions, um Dokumente mühelos im SVG-Format zu speichern. Vereinfachen Sie Ihren Workflow mit optimaler Dateiverwaltung!
type: docs
weight: 100
url: /de/net/aspose.words.saving/svgsaveoptions/saveformat/
---
## SvgSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurSvg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Beispiele

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
/// Zählt und druckt URIs der enthaltenen Ressourcen, wenn sie in .svg konvertiert werden.
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
