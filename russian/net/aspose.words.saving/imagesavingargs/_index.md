---
title: Class ImageSavingArgs
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.ImageSavingArgs сорт. Предоставляет данные дляImageSaving событие.
type: docs
weight: 5240
url: /ru/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Предоставляет данные для[`ImageSaving`](../iimagesavingcallback/imagesaving/) событие.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) статья документации.

```csharp
public class ImageSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Получает[`ShapeBase`](../../aspose.words.drawing/shapebase/) объект, соответствующий форме или группе фигур , которая будет сохранена. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Получает объект документа, который в данный момент сохраняется. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Получает или задает имя файла (без пути), в котором будет сохранено изображение. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Позволяет указать поток, в который будет сохранено изображение. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | Возвращает`истинный` если текущее изображение доступно для экспорта. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Указывает, должен ли Aspose.Words сохранять поток открытым или закрывать его после сохранения изображения. |

### Примечания

По умолчанию, когда Aspose.Words сохраняет документ в HTML, он сохраняет каждое изображение в в отдельный файл. Aspose.Words использует имя файла документа и уникальный номер для создания уникального имени файла для каждого изображения, найденного в документе.

`ImageSavingArgs`позволяет переопределить способ создания имен файлов изображений или полностью обойти сохранение изображений в файлы, предоставив свои собственные объекты потока.

Чтобы применить собственную логику для создания имен файлов изображений, используйте [`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) и[`IsImageAvailable`](./isimageavailable/) Свойства .

Чтобы сохранять изображения в потоки, а не в файлы, используйте команду[`ImageStream`](./imagestream/) свойство.

### Примеры

Показывает, как разделить документ на части и сохранить их.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Создаем объект HtmlFixedSaveOptions, который мы можем передать методу Save документа.
    // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Если мы сохраним документ как обычно, будет один выходной HTML
    // документ со всем содержимым исходного документа.
    // Установите для свойства DocumentSplitCriteria значение DocumentSplitCriteria.SectionBreak, чтобы
    // сохраняем наш документ в несколько HTML-файлов: по одному на каждый раздел.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Назначаем пользовательский обратный вызов свойству «DocumentPartSavingCallback», чтобы изменить логику сохранения части документа.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Если мы преобразуем документ, содержащий изображения, в HTML, мы получим один HTML-файл, который ссылается на несколько изображений.
    // Каждое изображение будет в виде файла в локальной файловой системе.
    // Существует также обратный вызов, который может настроить имя и расположение файловой системы каждого изображения.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Устанавливает собственные имена файлов для выходных документов, на которые операция сохранения разбивает документ.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Мы можем получить доступ ко всему исходному документу через свойство «Документ».
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
        // 1 - Установить имя файла выходной части:
        args.DocumentPartFileName = partFileName;

        // 2 - Создать собственный поток для файла выходной части:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Устанавливает собственные имена файлов изображений, создаваемых преобразованием HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
        // 1 - Установить имя файла выходного изображения:
        args.ImageFileName = imageFileName;

        // 2 — Создать собственный поток для выходного файла изображения:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


