---
title: ImageSavingArgs.ImageStream
second_title: Справочник по API Aspose.Words для .NET
description: ImageSavingArgs свойство. Позволяет указать поток в который будет сохранено изображение.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Позволяет указать поток, в который будет сохранено изображение.

```csharp
public Stream ImageStream { get; set; }
```

### Примечания

Это свойство позволяет сохранять изображения в потоки вместо файлов во время HTML.

Значение по умолчанию:`нулевой` . Когда это свойство`нулевой` , изображение будет сохранено в файл, указанный в[`ImageFileName`](../imagefilename/) свойство.

С использованием[`IImageSavingCallback`](../../iimagesavingcallback/) вы не можете заменить одно изображение другим. Он предназначен только для контроля над местом сохранения изображений.

### Примеры

Показывает, как включить обратный вызов сохранения изображения в процесс преобразования HTML.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions для обозначения обратного вызова
    // чтобы настроить процесс сохранения изображения.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Печатает свойства каждого изображения, поскольку процесс сохранения сохраняет его в файл изображения в локальной файловой системе.
/// при экспорте документа в HTML.
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
* пространство имен [Aspose.Words.Saving](../../imagesavingargs/)
* сборка [Aspose.Words](../../../)


