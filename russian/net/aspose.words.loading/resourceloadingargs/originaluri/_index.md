---
title: ResourceLoadingArgs.OriginalUri
linktitle: OriginalUri
articleTitle: OriginalUri
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ResourceLoadingArgs OriginalUri — получите доступ к исходному URI ресурсов из импортированных документов для оптимизированного управления данными.
type: docs
weight: 10
url: /ru/net/aspose.words.loading/resourceloadingargs/originaluri/
---
## ResourceLoadingArgs.OriginalUri property

Исходный URI ресурса, указанный в импортированном документе.

```csharp
public string OriginalUri { get; }
```

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

* class [ResourceLoadingArgs](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
