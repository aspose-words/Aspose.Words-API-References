---
title: IResourceLoadingCallback.ResourceLoading
linktitle: ResourceLoading
articleTitle: ResourceLoading
second_title: .NET için Aspose.Words
description: IResourceLoadingCallback'in, sorunsuz belge işleme için harici kaynak yüklemesini etkin bir şekilde yöneterek Aspose.Words'ü nasıl geliştirdiğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/iresourceloadingcallback/resourceloading/
---
## IResourceLoadingCallback.ResourceLoading method

Aspose.Words herhangi bir harici kaynağı yüklediğinde çağrılır.

```csharp
public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
```

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

* enum [ResourceLoadingAction](../../resourceloadingaction/)
* class [ResourceLoadingArgs](../../resourceloadingargs/)
* interface [IResourceLoadingCallback](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
