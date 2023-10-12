---
title: Interface IResourceLoadingCallback
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Loading.IResourceLoadingCallback интерфейс. Реализуйте этот интерфейс если хотите контролировать как Aspose.Words загружает внешний ресурс при импорте документа и вставке изображений с помощьюDocumentBuilder .
type: docs
weight: 3640
url: /ru/net/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface

Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words загружает внешний ресурс при импорте документа и вставке изображений с помощью[`DocumentBuilder`](../../aspose.words/documentbuilder/) .

```csharp
public interface IResourceLoadingCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [ResourceLoading](../../aspose.words.loading/iresourceloadingcallback/resourceloading/)(ResourceLoadingArgs) | Вызывается, когда Aspose.Words загружает любой внешний ресурс. |

### Примеры

Показывает, как настроить процесс загрузки внешних ресурсов в документ.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Изображения обычно вставляются с использованием URI или массива байтов.
    // Каждый экземпляр загрузки ресурса будет вызывать метод ResourceLoading нашего обратного вызова.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Позволяет нам загружать изображения в документ, используя предопределенные сокращения, а не URI.
/// Это позволит отделить логику загрузки изображения от остальной части конструкции документа.
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


