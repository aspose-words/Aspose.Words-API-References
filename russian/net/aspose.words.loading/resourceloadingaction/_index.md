---
title: ResourceLoadingAction Enum
linktitle: ResourceLoadingAction
articleTitle: ResourceLoadingAction
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.ResourceLoadingAction для эффективных режимов загрузки ресурсов. Улучшите обработку документов с оптимизированной производительностью!
type: docs
weight: 4140
url: /ru/net/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enumeration

Указывает режим загрузки ресурсов.

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) документальная статья.

```csharp
public enum ResourceLoadingAction
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Default | `0` | Aspose.Words загрузит этот ресурс как обычно. |
| Skip | `1` | Aspose.Words пропустит загрузку этого ресурса. Для изображения будет сохранена только ссылка без данных, таблица стилей CSS будет проигнорирована для формата HTML. |
| UserProvided | `2` | Aspose.Words будет использовать массив байтов, предоставленный пользователем в[`SetData`](../resourceloadingargs/setdata/) как данные ресурса. |

## Примеры

Показывает, как настроить процесс загрузки внешних ресурсов в документ.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Изображения обычно вставляются с помощью URI или байтового массива.
    // Каждый экземпляр загрузки ресурса будет вызывать метод ResourceLoading нашего обратного вызова.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Позволяет загружать изображения в документ, используя предопределенные сокращения, а не URI.
/// Это отделит логику загрузки изображения от остальной части конструкции документа.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Если этот обратный вызов встречает одно из сокращений изображения при загрузке изображения,
        // он будет применять уникальную логику для каждого определенного сокращения вместо того, чтобы рассматривать его как URI.
        if (args.ResourceType == ResourceType.Image)
            switch (args.OriginalUri)
            {
                case "Google logo":
                    using (WebClient webClient = new WebClient())
                    {
                        args.SetData(webClient.DownloadData("http://www.google.com/images/logos/ps_logo2.png"));
                    }

                    return ResourceLoadingAction.UserProvided;

                case "Aspose logo":
                    args.SetData(File.ReadAllBytes(ImageDir + "Logo.jpg"));

                    return ResourceLoadingAction.UserProvided;

                case "Watermark":
                    args.SetData(File.ReadAllBytes(ImageDir + "Transparent background logo.png"));

                    return ResourceLoadingAction.UserProvided;
            }

        return ResourceLoadingAction.Default;
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
