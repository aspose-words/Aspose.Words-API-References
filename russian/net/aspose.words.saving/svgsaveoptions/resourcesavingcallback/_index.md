---
title: SvgSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words для .NET
description: Управляйте экономией ресурсов изображения с помощью ResourceSavingCallback SvgSaveOptions. Оптимизируйте экспорт SVG для лучшего качества и эффективности.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/svgsaveoptions/resourcesavingcallback/
---
## SvgSaveOptions.ResourceSavingCallback property

Позволяет контролировать сохранение ресурсов (изображений) при экспорте документа в формат SVG.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
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

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
