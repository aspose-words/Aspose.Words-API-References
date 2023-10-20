---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words для .NET
description: ImageSavingArgs CurrentShape свойство. ПолучаетShapeBase объект соответствующий форме или группе фигур  которая будет сохранена на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Получает[`ShapeBase`](../../../aspose.words.drawing/shapebase/) объект, соответствующий форме или группе фигур , которая будет сохранена.

```csharp
public ShapeBase CurrentShape { get; }
```

## Примечания

[`IImageSavingCallback`](../../iimagesavingcallback/) может быть запущен при сохранении формы или формы группы. Вот почему в собственности есть[`ShapeBase`](../../../aspose.words.drawing/shapebase/) тип. Вы можете проверить, является ли это фигурой группы, сравнивая [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) сGroup или приведя его к одному из производных классов: [`Shape`](../../../aspose.words.drawing/shape/) или[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words использует имя файла документа и уникальный номер для создания уникального имени файла для каждого изображения, найденного в документе. Вы можете использовать`CurrentShape`свойство для создания «лучшего» имени файла путем изучения свойств формы, таких как[`Title`](../../../aspose.words.drawing/imagedata/title/) (только форма),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Только форма) и[`Name`](../../../aspose.words.drawing/shapebase/name/). Конечно, вы можете создавать имена файлов, используя любые другие свойства или критерии , но обратите внимание, что имена вспомогательных файлов должны быть уникальными в рамках операции экспорта.

Некоторые изображения в документе могут быть недоступны. Чтобы проверить доступность изображения , используйте команду[`IsImageAvailable`](../isimageavailable/) свойство.

## Примеры

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
