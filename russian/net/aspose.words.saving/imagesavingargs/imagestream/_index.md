---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageStream в ImageSavingArgs, чтобы легко указать место сохранения изображений, тем самым улучшив рабочий процесс и повысив эффективность.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Позволяет указать поток, в который будет сохранено изображение.

```csharp
public Stream ImageStream { get; set; }
```

## Примечания

Это свойство позволяет сохранять изображения в потоки, а не в файлы во время HTML.

Значение по умолчанию:`нулевой` . Когда это свойство`нулевой` , изображение будет сохранено в файле, указанном в[`ImageFileName`](../imagefilename/) свойство.

С использованием[`IImageSavingCallback`](../../iimagesavingcallback/) нельзя заменить одно изображение на другое. Он предназначен только для контроля места сохранения изображений.

## Примеры

Показывает, как включить обратный вызов сохранения изображения в процесс преобразования HTML.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions для назначения обратного вызова
    // для настройки процесса сохранения изображения.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Печатает свойства каждого изображения, поскольку процесс сохранения сохраняет его в файле изображения в локальной файловой системе.
/// во время экспорта документа в HTML.
/// </summary>
private class ImageShapePrinter : IImageSavingCallback
{
    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        args.KeepImageStreamOpen = false;
        Assert.True(args.IsImageAvailable);

        Console.WriteLine($"{args.Document.OriginalFileName.Split('\\').Last()} Image #{++mImageCount}");

        LayoutCollector layoutCollector = new LayoutCollector(args.Document);

        Console.WriteLine($"\tOn page:\t{layoutCollector.GetStartPageIndex(args.CurrentShape)}");
        Console.WriteLine($"\tDimensions:\t{args.CurrentShape.Bounds}");
        Console.WriteLine($"\tAlignment:\t{args.CurrentShape.VerticalAlignment}");
        Console.WriteLine($"\tWrap type:\t{args.CurrentShape.WrapType}");
        Console.WriteLine($"Output filename:\t{args.ImageFileName}\n");
    }

    private int mImageCount;
}
```

### Смотрите также

* class [ImageSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
