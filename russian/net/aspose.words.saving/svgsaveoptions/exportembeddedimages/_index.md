---
title: SvgSaveOptions.ExportEmbeddedImages
second_title: Справочник по API Aspose.Words для .NET
description: SvgSaveOptions свойство. Указывает следует ли встраивать изображения в документ SVG в формате base64. Обратите внимание что установка этого флага может значительно увеличить размер выходного файла SVG.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

Указывает, следует ли встраивать изображения в документ SVG в формате base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного файла SVG.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

### Примеры

Показывает, как управлять и печатать URI связанных ресурсов, созданных при преобразовании документа в .svg.

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
/// Подсчитывает и печатает URI ресурсов, содержащихся в, когда они преобразуются в .svg.
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

### Смотрите также

* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../svgsaveoptions/)
* сборка [Aspose.Words](../../../)


