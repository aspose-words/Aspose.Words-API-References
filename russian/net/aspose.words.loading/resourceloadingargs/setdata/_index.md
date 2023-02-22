---
title: ResourceLoadingArgs.SetData
second_title: Справочник по API Aspose.Words для .NET
description: ResourceLoadingArgs метод. Устанавливает предоставленные пользователем данные ресурса который используется  еслиResourceLoading возвращаетUserProvided .
type: docs
weight: 40
url: /ru/net/aspose.words.loading/resourceloadingargs/setdata/
---
## ResourceLoadingArgs.SetData method

Устанавливает предоставленные пользователем данные ресурса, который используется , если[`ResourceLoading`](../../iresourceloadingcallback/resourceloading/) возвращаетUserProvided .

```csharp
public void SetData(byte[] data)
```

### Примеры

Показывает, как настроить процесс загрузки внешних ресурсов в документ.

```csharp
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Изображения обычно вставляются с использованием URI или массива байтов.
    // Каждый экземпляр загрузки ресурсов будет вызывать метод ResourceLoading нашего обратного вызова.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");

/// <summary>
/// Позволяет нам загружать изображения в документ, используя предопределенные сокращения, а не URI.
/// Это отделит логику загрузки изображения от остальной конструкции документа.
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
* пространство имен [Aspose.Words.Loading](../../resourceloadingargs/)
* сборка [Aspose.Words](../../../)


