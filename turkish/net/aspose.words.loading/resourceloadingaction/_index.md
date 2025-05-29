---
title: ResourceLoadingAction Enum
linktitle: ResourceLoadingAction
articleTitle: ResourceLoadingAction
second_title: .NET için Aspose.Words
description: Verimli kaynak yükleme modları için Aspose.Words.ResourceLoadingAction enum'unu keşfedin. Optimize edilmiş performansla belge işlemenizi geliştirin!
type: docs
weight: 4140
url: /tr/net/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enumeration

Kaynak yükleme modunu belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-load-options/) belgeleme makalesi.

```csharp
public enum ResourceLoadingAction
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Default | `0` | Aspose.Words bu kaynağı her zamanki gibi yükleyecektir. |
| Skip | `1` | Aspose.Words bu kaynağın yüklenmesini atlayacaktır. Bir resim için yalnızca veri içermeyen bağlantı saklanacaktır, HTML biçimi için CSS stil sayfası yoksayılacaktır. |
| UserProvided | `2` | Aspose.Words, kullanıcı tarafından sağlanan bayt dizisini kullanacaktır.[`SetData`](../resourceloadingargs/setdata/) kaynak verisi olarak. |

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
