---
title: ImageSavingArgs Class
linktitle: ImageSavingArgs
articleTitle: ImageSavingArgs
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.ImageSavingArgs, улучшающий обработку документов с помощью настраиваемых параметров сохранения изображений для оптимальной производительности.
type: docs
weight: 5990
url: /ru/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Предоставляет данные для[`ImageSaving`](../iimagesavingcallback/imagesaving/) событие.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class ImageSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Получает[`ShapeBase`](../../aspose.words.drawing/shapebase/) объект, соответствующий форме или групповой форме , которая будет сохранена. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Получает объект документа, который в данный момент сохраняется. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Возвращает или задает имя файла (без пути), в котором будет сохранено изображение. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Позволяет указать поток, в который будет сохранено изображение. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | Возврат`истинный` если текущее изображение доступно для экспорта. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Указывает, должен ли Aspose.Words держать поток открытым или закрыть его после сохранения изображения. |

## Примечания

По умолчанию, когда Aspose.Words сохраняет документ в HTML, он сохраняет каждое изображение в отдельный файл. Aspose.Words использует имя файла документа и уникальный номер для генерации уникального имени файла для каждого изображения, найденного в документе.

`ImageSavingArgs`позволяет переопределить способ генерации имен файлов изображений или полностью обойти сохранение изображений в файлы, предоставив собственные потоковые объекты.

Чтобы применить собственную логику для генерации имен файлов изображений, используйте [`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) и[`IsImageAvailable`](./isimageavailable/) свойства.

Чтобы сохранять изображения в потоки, а не в файлы, используйте[`ImageStream`](./imagestream/) свойство.

## Примеры

Показывает, как разделить документ на части и сохранить их.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Создаем объект "HtmlFixedSaveOptions", который можно передать методу "Save" документа
    // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Если мы сохраним документ обычным образом, будет один выходной HTML
    // документ со всем содержимым исходного документа.
    // Установите свойство "DocumentSplitCriteria" в "DocumentSplitCriteria.SectionBreak" для
    // сохраняем наш документ в несколько HTML-файлов: по одному для каждого раздела.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Назначьте пользовательский обратный вызов свойству "DocumentPartSavingCallback", чтобы изменить логику сохранения части документа.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Если мы преобразуем документ, содержащий изображения, в html, мы получим один html-файл, который ссылается на несколько изображений.
    // Каждое изображение будет иметь форму файла в локальной файловой системе.
    // Также имеется обратный вызов, который позволяет настраивать имя и местоположение каждого изображения в файловой системе.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Задает пользовательские имена файлов для выходных документов, на которые операция сохранения разбивает документ.
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

        // Ниже приведены два способа указания того, где Aspose.Words будет сохранять каждую часть документа.
        // 1 - Задайте имя файла для выходного файла детали:
        args.DocumentPartFileName = partFileName;

        // 2 - Создать пользовательский поток для выходного файла детали:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Задает пользовательские имена файлов изображений, создаваемых при преобразовании HTML.
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

        // Ниже приведены два способа указания того, где Aspose.Words будет сохранять каждую часть документа.
        // 1 — Задайте имя файла для выходного изображения:
        args.ImageFileName = imageFileName;

        // 2 — Создать пользовательский поток для выходного файла изображения:
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
