---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: Aspose.Words для .NET
description: Проверьте, готово ли изображение к экспорту, с помощью свойства IsImageAvailable в ImageSavingArgs. Обеспечьте бесперебойное управление изображениями и эффективность!
type: docs
weight: 50
url: /ru/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Возврат`истинный` если текущее изображение доступно для экспорта.

```csharp
public bool IsImageAvailable { get; }
```

## Примечания

Некоторые изображения в документе могут быть недоступны, например, потому что image связано, а ссылка недоступна или не указывает на допустимое изображение. В этом случае Aspose.Words экспортирует значок с красным крестом. Это свойство возвращает `истинный` если исходное изображение доступно; возвращает`ЛОЖЬ`если исходное изображение недоступно, для сохранения будет предложен значок «нет изображения».

При сохранении групповой фигуры или фигуры, не требующей изображения, это свойство всегда`истинный`.

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
