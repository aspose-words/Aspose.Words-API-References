---
title: SvgSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SvgSaveOptions SaveFormat, чтобы без усилий сохранять документы в формате SVG. Упростите свой рабочий процесс с помощью оптимального управления файлами!
type: docs
weight: 100
url: /ru/net/aspose.words.saving/svgsaveoptions/saveformat/
---
## SvgSaveOptions.SaveFormat property

Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоSvg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Примеры

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
/// Подсчитывает и выводит URI ресурсов, содержащихся в, по мере их преобразования в .svg.
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
