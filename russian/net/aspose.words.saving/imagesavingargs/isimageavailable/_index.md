---
title: ImageSavingArgs.IsImageAvailable
second_title: Справочник по API Aspose.Words для .NET
description: ImageSavingArgs свойство. Возвращаетистинный если текущее изображение доступно для экспорта.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Возвращает`истинный` если текущее изображение доступно для экспорта.

```csharp
public bool IsImageAvailable { get; }
```

### Примечания

Некоторые изображения в документе могут быть недоступны, например, потому, что ссылка image недоступна или не указывает на действительное изображение. В этом случае Aspose.Words экспортирует значок с красным крестом. Это свойство возвращает `истинный` доступно ли исходное изображение; возвращает`ЛОЖЬ`если исходное изображение недоступно и для сохранения будет предложен значок «нет изображения».

При сохранении фигуры группы или фигуры, не требующей изображения, это свойство всегда имеет значение.`истинный`.

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../imagesavingargs/)
* сборка [Aspose.Words](../../../)


