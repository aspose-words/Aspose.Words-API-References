---
title: SvgSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Eigenschaft „SvgSaveOptions ExportEmbeddedImages“ Bilder als Base64 in SVG-Dateien einbetten und so die Portabilität verbessern und gleichzeitig die Dateigröße verwalten können.
type: docs
weight: 20
url: /de/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

Gibt an, ob Bilder als Base64 in das SVG-Dokument eingebettet werden sollen. Beachten Sie, dass das Aktivieren dieser Option zu einer erheblichen Vergrößerung der SVG-Ausgabedatei führen kann.

```csharp
public bool ExportEmbeddedImages { get; set; }
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

* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
