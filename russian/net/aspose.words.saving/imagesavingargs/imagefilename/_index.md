---
title: ImageFileName
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает имя файла без пути в котором будет сохранено изображение.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/imagesavingargs/imagefilename/
---
## ImageSavingArgs.ImageFileName property

Получает или задает имя файла (без пути), в котором будет сохранено изображение.

```csharp
public string ImageFileName { get; set; }
```

### Примечания

Это свойство позволяет переопределить способ генерации имен файлов изображений во время экспорта в HTML.

Когда событие запускается, это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить изображение в другом файле. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного изображения при экспорте в формат HTML. Способ генерации имени файла изображения зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла изображения выглядит как &lt;имя файла базы документов&gt;.&lt;номер изображения&gt;.&lt;расширение&gt;.

При сохранении документа в поток сгенерированное имя файла изображения выглядит как Aspose.Words.&lt;guid документа&gt;.&lt;номер изображения&gt;.&lt;расширение&gt;.

`ImageFileName` должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения и значение`источник`атрибут для записи в HTML с использованием имени файла документа,[`ImagesFolder`](../../htmlsaveoptions/imagesfolder) и [`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias) характеристики.

### Примеры

Показывает, как разделить документ на части и сохранить их.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Создаем объект "HtmlFixedSaveOptions", который мы можем передать в метод документа "Сохранить"
    // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Если мы сохраним документ нормально, будет один выходной HTML
    // документ со всем содержимым исходного документа.
    // Установите для свойства "DocumentSplitCriteria" значение "DocumentSplitCriteria.SectionBreak", чтобы
    // сохраняем наш документ в несколько файлов HTML: по одному на каждый раздел.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Назначаем пользовательский обратный вызов свойству «DocumentPartSavingCallback», чтобы изменить логику сохранения части документа.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Если мы преобразуем документ, содержащий изображения, в html, мы получим один html-файл, который ссылается на несколько изображений.
    // Каждое изображение будет в виде файла в локальной файловой системе.
    // Существует также обратный вызов, который может настроить имя и местоположение в файловой системе каждого изображения.
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

        // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
        // 1 - Установить имя файла для выходного файла детали:
        args.DocumentPartFileName = partFileName;

        // 2 - Создайте пользовательский поток для файла выходной части:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Устанавливает пользовательские имена файлов для файлов изображений, которые создаются при преобразовании HTML.
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

        // 2 - Создайте пользовательский поток для выходного файла изображения:
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

* class [ImageSavingArgs](../../imagesavingargs)
* пространство имен [Aspose.Words.Saving](../../imagesavingargs)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
