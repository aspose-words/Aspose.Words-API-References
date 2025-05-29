---
title: ResourceSavingArgs.ResourceFileName
linktitle: ResourceFileName
articleTitle: ResourceFileName
second_title: Aspose.Words для .NET
description: Эффективно управляйте своими ресурсами с помощью ResourceSavingArgs. Легко задайте или получите имя файла для сохранения ресурсов без хлопот с путями.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

Возвращает или задает имя файла (без пути), в котором будет сохранен ресурс.

```csharp
public string ResourceFileName { get; set; }
```

## Примечания

Это свойство позволяет переопределить способ генерации имен файлов ресурсов во время экспорта в фиксированный HTML-файл страницы или SVG.

При запуске события это свойство содержит имя файла, сгенерированное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить ресурс в другом файле. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого ресурса при экспорте в формат HTML или SVG с фиксированной страницей. То, как генерируется имя файла ресурса , зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла ресурса выглядит как &lt;имя файла базы документа&gt;.&lt;номер изображения&gt;.&lt;расширение&gt;.

При сохранении документа в потоке сгенерированное имя файла ресурса выглядит как Aspose.Words.&lt;guid документа&gt;.&lt;номер изображения&gt;.&lt;расширение&gt;.

`ResourceFileName` должно содержать только имя файла без пути. Aspose.Words определяет путь для сохранения и значение`источник` атрибут для записи в фиксированную страницу HTML или SVG с использованием имени файла документа,[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) или[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) и[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) или[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) характеристики.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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

* class [ResourceSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
