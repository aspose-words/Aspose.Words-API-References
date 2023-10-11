---
title: SvgSaveOptions.ResourcesFolder
second_title: Aspose.Words für .NET-API-Referenz
description: SvgSaveOptions eigendom. Gibt den physischen Ordner an in dem Ressourcen Bilder gespeichert werden wenn ein Dokument in das SVGFormat exportiert wird. Standard istNull .
type: docs
weight: 50
url: /de/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Gibt den physischen Ordner an, in dem Ressourcen (Bilder) gespeichert werden, wenn ein Dokument in das SVG-Format exportiert wird. Standard ist`Null` .

```csharp
public string ResourcesFolder { get; set; }
```

### Bemerkungen

Hat nur Wirkung, wenn[`ExportEmbeddedImages`](../exportembeddedimages/) Eigentum ist`FALSCH`.

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) Im SVG-Format muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.`ResourcesFolder` Mit können Sie angeben, wo die Bilder gespeichert werden[`ResourcesFolderAlias`](../resourcesfolderalias/) ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words standardmäßig die -Bilder im selben Ordner, in dem die Dokumentdatei gespeichert ist. Verwenden`ResourcesFolder` , um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words nicht über einen Ordner zum Speichern der Bilder, , muss die Bilder aber dennoch irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner im angeben`ResourcesFolder` Eigentum

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
/// Zählt und druckt die URIs der darin enthaltenen Ressourcen, während sie in .svg konvertiert werden.
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
* namensraum [Aspose.Words.Saving](../../svgsaveoptions/)
* Montage [Aspose.Words](../../../)


