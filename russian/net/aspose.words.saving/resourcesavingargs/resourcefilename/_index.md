---
title: ResourceSavingArgs.ResourceFileName
second_title: Справочник по API Aspose.Words для .NET
description: ResourceSavingArgs свойство. Получает или задает имя файла без пути в котором будет сохранен ресурс.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

Получает или задает имя файла (без пути), в котором будет сохранен ресурс.

```csharp
public string ResourceFileName { get; set; }
```

### Примечания

Это свойство позволяет переопределить способ генерации имен файлов ресурсов во время экспорта в HTML или SVG с фиксированной страницей.

Когда событие запускается, это свойство содержит имя файла , созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить ресурс в другом файле . Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого ресурса при экспорте в формат фиксированной страницы HTML или SVG. Способ создания имени файла ресурса зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл имя сгенерированного файла ресурсов выглядит как .&lt;имя файла базы документов&gt;.&lt;номер образа&gt;.&lt;расширение&gt;.

При сохранении документа в поток имя сгенерированного файла ресурсов выглядит как .Aspose.Words.&lt;руководство документа&gt;.&lt;номер изображения&gt;.&lt;расширение&gt;.

`ResourceFileName` должно содержать только имя файла без пути. Aspose.Words определяет путь для сохранения и значение параметра`источник` атрибут для записи на фиксированную страницу HTML или SVG с использованием имени файла документа,[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) или[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) и[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) или[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) характеристики.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

### Примеры

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
    /// Вызывается, когда Aspose.Words сохраняет внешний ресурс в HTML или SVG фиксированной страницы.
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
* пространство имен [Aspose.Words.Saving](../../resourcesavingargs/)
* сборка [Aspose.Words](../../../)


