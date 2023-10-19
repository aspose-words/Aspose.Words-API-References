---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: Aspose.Words for .NET
description: Aspose.Words.Loading.ResourceLoadingArgs sınıf. Şunun için veri sağlarResourceLoading yöntem C#'da.
type: docs
weight: 3690
url: /tr/net/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class

Şunun için veri sağlar:[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) yöntem.

```csharp
public class ResourceLoadingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | İçe aktarılan belgede belirtildiği şekliyle kaynağın orijinal URI'si. |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | Kaynak türü. |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | İndirmek için kullanılan kaynağın URI'si ise[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) şunu döndürürDefault. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | Aşağıdaki durumlarda kullanılan kaynağın kullanıcı tarafından sağlanan verilerini ayarlar:[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) şunu döndürürUserProvided . |

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

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
