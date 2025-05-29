---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie den ResourcesFolder in SvgSaveOptions für eine effiziente Bildspeicherung beim Exportieren von Dokumenten ins SVG-Format festlegen. Optimieren Sie noch heute Ihren Workflow!
type: docs
weight: 80
url: /de/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Gibt den physischen Ordner an, in dem Ressourcen (Bilder) beim Exportieren eines Dokuments in das SVG-Format gespeichert werden. Standard ist`null` .

```csharp
public string ResourcesFolder { get; set; }
```

## Bemerkungen

Wirkt nur, wenn[`ExportEmbeddedImages`](../exportembeddedimages/) Eigentum ist`FALSCH`.

Wenn Sie eine[`Document`](../../../aspose.words/document/) Im SVG-Format muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.`ResourcesFolder` ermöglicht Ihnen, festzulegen, wo die Bilder gespeichert werden und[`ResourcesFolderAlias`](../resourcesfolderalias/) ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words die -Bilder standardmäßig im selben Ordner wie die Dokumentdatei. Verwenden Sie`ResourcesFolder` , um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words nicht über einen Ordner, in dem die Bilder gespeichert werden können, , muss die Bilder aber trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner in der`ResourcesFolder` Eigentum

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
