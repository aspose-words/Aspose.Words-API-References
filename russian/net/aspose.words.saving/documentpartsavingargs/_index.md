---
title: DocumentPartSavingArgs Class
linktitle: DocumentPartSavingArgs
articleTitle: DocumentPartSavingArgs
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.DocumentPartSavingArgs, необходимый для улучшения обработки документов с помощью настраиваемых параметров сохранения и эффективных обратных вызовов.
type: docs
weight: 5690
url: /ru/net/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class

Предоставляет данные для[`DocumentPartSaving`](../idocumentpartsavingcallback/documentpartsaving/) обратный вызов.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class DocumentPartSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.saving/documentpartsavingargs/document/) { get; } | Получает объект документа, который сохраняется. |
| [DocumentPartFileName](../../aspose.words.saving/documentpartsavingargs/documentpartfilename/) { get; set; } | Возвращает или задает имя файла (без пути), в котором будет сохранена часть документа. |
| [DocumentPartStream](../../aspose.words.saving/documentpartsavingargs/documentpartstream/) { get; set; } | Позволяет указать поток, в который будет сохранена часть документа. |
| [KeepDocumentPartStreamOpen](../../aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/) { get; set; } | Указывает, должен ли Aspose.Words держать поток открытым или закрыть его после сохранения части документа. |

## Примечания

Когда Aspose.Words сохраняет документ в HTML или связанных форматах и[`DocumentSplitCriteria`](../htmlsaveoptions/documentsplitcriteria/)Если указано , документ разбивается на части и по умолчанию каждая часть документа сохраняется в отдельный файл.

Сорт`DocumentPartSavingArgs` позволяет вам контролировать, как будет сохранена каждая часть документа. Позволяет переопределить способ генерации имен файлов или полностью обойти сохранение частей документа в файлы , предоставив собственные потоковые объекты.

Чтобы сохранить части документа в потоки, а не в файлы, используйте[`DocumentPartStream`](./documentpartstream/) свойство.

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
