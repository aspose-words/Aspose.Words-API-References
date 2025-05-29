---
title: ImageSavingArgs.KeepImageStreamOpen
linktitle: KeepImageStreamOpen
articleTitle: KeepImageStreamOpen
second_title: Aspose.Words для .NET
description: Откройте для себя свойство KeepImageStreamOpen в ImageSavingArgs для Aspose.Words. Управляйте поведением потока для эффективного сохранения изображений и повышения производительности.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

Указывает, должен ли Aspose.Words держать поток открытым или закрыть его после сохранения изображения.

```csharp
public bool KeepImageStreamOpen { get; set; }
```

## Примечания

По умолчанию`ЛОЖЬ` и Aspose.Words закроет предоставленный вами поток в[`ImageStream`](../imagestream/) свойство после записи в него изображения. Укажите`истинный` чтобы поток оставался открытым.

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
