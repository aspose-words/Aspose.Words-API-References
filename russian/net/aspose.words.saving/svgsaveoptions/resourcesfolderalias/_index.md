---
title: SvgSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SvgSaveOptions ResourcesFolderAlias для настройки URI изображений в документах SVG. Улучшите свой вывод SVG с помощью гибкого именования папок!
type: docs
weight: 90
url: /ru/net/aspose.words.saving/svgsaveoptions/resourcesfolderalias/
---
## SvgSaveOptions.ResourcesFolderAlias property

Указывает имя папки, используемой для создания URI изображений, записанных в документ SVG. Значение по умолчанию:`нулевой` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате SVG Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы.[`ResourcesFolder`](../resourcesfolder/) позволяет указать, где будут сохранены изображения и`ResourcesFolderAlias` позволяет указать, как будут формироваться URI изображений.

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

* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
