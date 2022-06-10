---
title: DocumentPartSavingCallback
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет управлять сохранением частей документа при сохранении документа в формате HTML или EPUB.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/
---
## HtmlSaveOptions.DocumentPartSavingCallback property

Позволяет управлять сохранением частей документа при сохранении документа в формате HTML или EPUB.

```csharp
public IDocumentPartSavingCallback DocumentPartSavingCallback { get; set; }
```

### Примеры

Показывает, как разделить документ на части и сохранить их.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Создаем объект «HtmlFixedSaveOptions», который мы можем передать в метод «Сохранить» документа method
     // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

     // Если мы сохраним документ нормально, будет один вывод HTML
     // документ со всем содержимым исходного документа.
    // Установите для свойства "DocumentSplitCriteria" значение "DocumentSplitCriteria.SectionBreak" to
     // сохраняем наш документ в несколько файлов HTML: по одному на каждый раздел.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

     // Назначаем пользовательский обратный вызов свойству «DocumentPartSavingCallback», чтобы изменить логику сохранения части документа.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

     // Если мы преобразуем документ, содержащий изображения, в html, мы получим один html-файл, который ссылается на несколько изображений.
     // Каждое изображение будет в виде файла в локальной файловой системе.
     // Существует также обратный вызов, который может настроить имя и местоположение файловой системы для каждого изображения.
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
         // Мы можем получить доступ ко всему исходному документу через свойство "Документ".
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
         // 1 - Установить имя файла для выходного файла части: 
        args.DocumentPartFileName = partFileName;

         // 2 - Создать пользовательский поток для файла выходной части: 
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

         // 2 - Создать пользовательский поток для выходного файла изображения: 
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

* interface [IDocumentPartSavingCallback](../../idocumentpartsavingcallback)
* class [HtmlSaveOptions](../../htmlsaveoptions)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
