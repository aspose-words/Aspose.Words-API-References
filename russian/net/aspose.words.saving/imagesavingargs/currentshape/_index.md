---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSavingArgs CurrentShape для доступа к объекту ShapeBase для эффективного сохранения фигур и групп фигур в ваших проектах.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Получает[`ShapeBase`](../../../aspose.words.drawing/shapebase/) объект, соответствующий форме или групповой форме , которая будет сохранена.

```csharp
public ShapeBase CurrentShape { get; }
```

## Примечания

[`IImageSavingCallback`](../../iimagesavingcallback/) может быть запущен при сохранении либо фигуры, либо групповой фигуры. Вот почему свойство имеет[`ShapeBase`](../../../aspose.words.drawing/shapebase/) тип. Вы можете проверить, является ли это групповой формой, сравнивая [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) сGroup или путем приведения его к одному из производных классов: [`Shape`](../../../aspose.words.drawing/shape/) или[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words использует имя файла документа и уникальный номер для генерации уникального имени файла для каждого изображения, найденного в документе. Вы можете использовать`CurrentShape`свойство для генерации «лучшего» имени файла путем изучения свойств формы, таких как[`Title`](../../../aspose.words.drawing/imagedata/title/) (только форма),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Только форма) и[`Name`](../../../aspose.words.drawing/shapebase/name/). Конечно, вы можете создавать имена файлов, используя любые другие свойства или критерии , но учтите, что имена дополнительных файлов должны быть уникальными в пределах операции экспорта.

Некоторые изображения в документе могут быть недоступны. Для проверки доступности изображения используйте[`IsImageAvailable`](../isimageavailable/) свойство.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
