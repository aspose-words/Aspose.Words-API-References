---
title: ResourceSavingArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ResourceSavingArgs Document для доступа к текущему сохраняемому объекту документа, что повысит эффективность вашего рабочего процесса.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/resourcesavingargs/document/
---
## ResourceSavingArgs.Document property

Получает объект документа, который в данный момент сохраняется.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [ResourceSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
