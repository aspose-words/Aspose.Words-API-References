---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words для .NET
description: Узнайте, как настроить ResourcesFolder в SvgSaveOptions для эффективного хранения изображений при экспорте документов в формат SVG. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 80
url: /ru/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Указывает физическую папку, в которой сохраняются ресурсы (изображения) при экспорте документа в формат SVG. Значение по умолчанию:`нулевой` .

```csharp
public string ResourcesFolder { get; set; }
```

## Примечания

Имеет эффект только если[`ExportEmbeddedImages`](../exportembeddedimages/) собственность есть`ЛОЖЬ`.

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате SVG Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы.`ResourcesFolder` позволяет указать, где будут сохранены изображения и[`ResourcesFolderAlias`](../resourcesfolderalias/) позволяет указать, как будут формироваться URI изображений.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения the в той же папке, где сохранен файл документа. Используйте`ResourcesFolder` для переопределения этого поведения.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки, куда можно сохранять изображения, , но все равно должен сохранять изображения где-то. В этом случае вам нужно указать доступную папку в`ResourcesFolder` свойство

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
