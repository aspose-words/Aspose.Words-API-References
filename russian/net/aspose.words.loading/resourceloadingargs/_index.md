---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Loading.ResourceLoadingArgs, разработанный для повышения эффективности загрузки ресурсов в ваших приложениях. Откройте для себя бесшовную интеграцию сегодня!
type: docs
weight: 4150
url: /ru/net/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class

Предоставляет данные для[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) метод.

```csharp
public class ResourceLoadingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | Исходный URI ресурса, указанный в импортированном документе. |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | Тип ресурса. |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | URI ресурса, который используется для загрузки , если[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) возвращаетDefault. |

## Методы

| Имя | Описание |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | Устанавливает предоставленные пользователем данные ресурса, который используется , если[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) возвращаетUserProvided . |

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
