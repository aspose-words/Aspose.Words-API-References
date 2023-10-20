---
title: SvgSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: Aspose.Words для .NET
description: SvgSaveOptions ResourcesFolderAlias свойство. Указывает имя папки используемой для создания URI изображений записываемых в документ SVG. Значение по умолчаниюнулевой  на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/svgsaveoptions/resourcesfolderalias/
---
## SvgSaveOptions.ResourcesFolderAlias property

Указывает имя папки, используемой для создания URI изображений, записываемых в документ SVG. Значение по умолчанию:`нулевой` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате SVG Aspose.Words необходимо сохранить изображения all , встроенные в документ, как отдельные файлы.[`ResourcesFolder`](../resourcesfolder/) позволяет указать, где будут сохраняться изображения и`ResourcesFolderAlias` позволяет указать, как будут создаваться URI изображения.

## Примеры

Показывает, как манипулировать и печатать URI связанных ресурсов, созданных при преобразовании документа в SVG.

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
/// Подсчитывает и печатает URI ресурсов, содержащихся в файле, при их преобразовании в .svg.
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
