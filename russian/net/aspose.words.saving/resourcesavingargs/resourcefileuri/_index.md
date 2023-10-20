---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words для .NET
description: ResourceSavingArgs ResourceFileUri свойство. Получает или задает универсальный идентификатор ресурса URI используемый для ссылки на файл ресурсов из документа на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Получает или задает универсальный идентификатор ресурса (URI), используемый для ссылки на файл ресурсов из документа.

```csharp
public string ResourceFileUri { get; set; }
```

## Примечания

Это свойство позволяет изменять URI файлов ресурсов, экспортированных в документы HTML или SVG с фиксированной страницей.

Aspose.Words автоматически генерирует URI для каждого файла ресурсов во время экспорта в формат фиксированной страницы HTML или SVG. Сгенерированные URI ссылаются на файлы ресурсов, сохраненные Aspose.Words. Однако URI могут быть неверными, если файлы ресурсов необходимо переместить в другое место или если файлы ресурсов сохраняются в потоках. Это свойство позволяет исправлять URI в таких случаях.

Когда событие запускается, это свойство содержит URI, созданный Aspose.Words. Вы можете изменить значение этого свойства, чтобы предоставить собственный URI для файла ресурсов.

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
