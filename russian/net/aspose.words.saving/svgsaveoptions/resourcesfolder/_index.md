---
title: SvgSaveOptions.ResourcesFolder
second_title: Справочник по API Aspose.Words для .NET
description: SvgSaveOptions свойство. Указывает физическую папку в которой сохраняются ресурсы изображения при экспорте документа в формат Svg. Значение по умолчаниюнулевой .
type: docs
weight: 50
url: /ru/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Указывает физическую папку, в которой сохраняются ресурсы (изображения) при экспорте документа в формат Svg. Значение по умолчанию:`нулевой` .

```csharp
public string ResourcesFolder { get; set; }
```

### Примечания

Имеет эффект только в том случае, если[`ExportEmbeddedImages`](../exportembeddedimages/) собственность`ЛОЖЬ`.

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате SVG Aspose.Words необходимо сохранить изображения all , встроенные в документ, как отдельные файлы.`ResourcesFolder` позволяет указать, где будут сохраняться изображения и[`ResourcesFolderAlias`](../resourcesfolderalias/) позволяет указать, как будут создаваться URI изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения the в той же папке, где сохраняется файл документа. Использовать`ResourcesFolder` , чтобы переопределить это поведение.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки для сохранения изображений, , но все равно необходимо где-то сохранять изображения. В этом случае вам необходимо указать доступную папку в поле`ResourcesFolder` свойство

### Примеры

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
* пространство имен [Aspose.Words.Saving](../../svgsaveoptions/)
* сборка [Aspose.Words](../../../)


