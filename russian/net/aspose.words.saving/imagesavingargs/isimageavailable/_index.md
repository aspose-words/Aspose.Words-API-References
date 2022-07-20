---
title: IsImageAvailable
second_title: Справочник по API Aspose.Words для .NET
description: Возвращаетистинный если текущее изображение доступно для экспорта.
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

Некоторые изображения в документе могут быть недоступны, например, из-за того, что изображение связано, а ссылка недоступна или не указывает на действительное изображение. В этом случае Aspose.Words экспортирует значок с красным крестом. Это свойство возвращает `истинный` доступно ли исходное изображение; возвращается`ЛОЖЬ` если исходное изображение недоступно и для сохранения будет предложен значок "нет изображения".

При сохранении групповой фигуры или фигуры, не требующей изображения, это свойство всегда`истинный`.

### Примеры

Показывает, как использовать обратный вызов сохранения изображения в процессе преобразования HTML.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions для назначения обратного вызова
    // для настройки процесса сохранения изображения.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Выводит свойства каждого изображения по мере того, как процесс сохранения сохраняет его в файл изображения в локальной файловой системе
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

* property [CurrentShape](../currentshape)
* class [ImageSavingArgs](../../imagesavingargs)
* пространство имен [Aspose.Words.Saving](../../imagesavingargs)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->