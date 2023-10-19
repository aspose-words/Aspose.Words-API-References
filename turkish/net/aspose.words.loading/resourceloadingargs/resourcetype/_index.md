---
title: ResourceLoadingArgs.ResourceType
linktitle: ResourceType
articleTitle: ResourceType
second_title: Aspose.Words for .NET
description: ResourceLoadingArgs ResourceType mülk. Kaynak türü C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.loading/resourceloadingargs/resourcetype/
---
## ResourceLoadingArgs.ResourceType property

Kaynak türü.

```csharp
public ResourceType ResourceType { get; }
```

## Örnekler

Dış kaynakları bir belgeye yükleme işleminin nasıl özelleştirileceğini gösterir.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Görüntüler genellikle bir URI veya bir bayt dizisi kullanılarak eklenir.
    // Bir kaynak yükünün her örneği, geri çağırmamızın ResourceLoading yöntemini çağıracaktır.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// URI'lerin aksine, önceden tanımlanmış kısayolları kullanarak görüntüleri bir belgeye yüklememize olanak tanır.
/// Bu, görüntü yükleme mantığını belge yapısının geri kalanından ayıracaktır.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Bu geri arama, bir görüntüyü yüklerken görüntünün kısa yollarından biriyle karşılaşırsa,
        // tanımlanan her kısayol için, onu bir URI olarak ele almak yerine benzersiz bir mantık uygulayacaktır.
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

### Ayrıca bakınız

* enum [ResourceType](../../resourcetype/)
* class [ResourceLoadingArgs](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
