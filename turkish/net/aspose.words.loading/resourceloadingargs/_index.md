---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: .NET için Aspose.Words
description: Uygulamalarınızda kaynak yükleme verimliliğini artırmak için tasarlanmış Aspose.Words.Loading.ResourceLoadingArgs sınıfını keşfedin. Bugün kusursuz entegrasyonun kilidini açın!
type: docs
weight: 4150
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
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | İçe aktarılan belgede belirtilen kaynağın orijinal URI'si. |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | Kaynak türü. |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | indirmek için kullanılan kaynağın URI'si[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) dönerDefault. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | Kullanılan kaynağın kullanıcı tarafından sağlanan verilerini ayarlar eğer[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) dönerUserProvided . |

## Örnekler

Harici kaynakların bir belgeye yüklenme sürecinin nasıl özelleştirileceğini gösterir.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Resimler genellikle bir URI veya bayt dizisi kullanılarak eklenir.
    // Kaynak yüklemesinin her örneği geri aramamızın ResourceLoading metodunu çağıracaktır.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// URI'lerin aksine, önceden tanımlanmış kısayollar kullanarak bir belgeye resim yüklememize olanak tanır.
/// Bu, görüntü yükleme mantığını belge yapısının geri kalanından ayıracaktır.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Bu geri çağırma, bir resim yüklenirken resim kısayollarından biriyle karşılaşırsa,
        // Tanımlanan her kısaltmayı bir URI olarak ele almak yerine, ona özgü bir mantık uygulayacaktır.
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
