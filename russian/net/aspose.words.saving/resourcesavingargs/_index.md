---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.ResourceSavingArgs, который улучшает обработку документов, предоставляя необходимые данные для события ResourceSaving.
type: docs
weight: 6360
url: /ru/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Предоставляет данные для[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) событие.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class ResourceSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Получает объект документа, который в данный момент сохраняется. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Указывает, должен ли Aspose.Words держать поток открытым или закрыть его после сохранения ресурса. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Возвращает или задает имя файла (без пути), в котором будет сохранен ресурс. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Возвращает или задает унифицированный идентификатор ресурса (URI), используемый для ссылки на файл ресурса из документа. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Позволяет указать поток, в который будет сохранен ресурс. |

## Примечания

По умолчанию, когда Aspose.Words сохраняет документ в HTML или SVG с фиксированной страницей, он сохраняет каждый ресурс в отдельный файл. Aspose.Words использует имя файла документа и уникальный номер для генерации уникального имени файла для каждого ресурса, найденного в документе.

`ResourceSavingArgs` позволяет переопределить способ генерации имен файлов ресурсов или полностью обойти сохранение ресурсов в файлы, предоставив собственные потоковые объекты.

Чтобы применить собственную логику для генерации имен файлов ресурсов, используйте [`ResourceFileName`](./resourcefilename/) свойство.

Чтобы сохранить ресурсы в потоки, а не в файлы, используйте[`ResourceStream`](./resourcestream/) свойство.

## Примеры

Показывает, как использовать обратный вызов для отслеживания внешних ресурсов, созданных при преобразовании документа в HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// Вызывается, когда Aspose.Words сохраняет внешний ресурс в формате HTML или SVG фиксированной страницы.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
