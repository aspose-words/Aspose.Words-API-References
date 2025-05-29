---
title: LoadOptions.ResourceLoadingCallback
linktitle: ResourceLoadingCallback
articleTitle: ResourceLoadingCallback
second_title: .NET için Aspose.Words
description: LoadOptions' ResourceLoadingCallback ile belge içe aktarımlarınızı optimize edin. Görüntüler ve stil sayfaları gibi harici kaynakların yüklenmesini sorunsuz bir şekilde kontrol edin.
type: docs
weight: 140
url: /tr/net/aspose.words.loading/loadoptions/resourceloadingcallback/
---
## LoadOptions.ResourceLoadingCallback property

Bir belge HTML veya MHTML'den içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmenizi sağlar.

```csharp
public IResourceLoadingCallback ResourceLoadingCallback { get; set; }
```

## Örnekler

Html belgeleri yüklenirken harici kaynakların nasıl kullanılacağını gösterir.

```csharp
public void LoadOptionsCallback()
{
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.ResourceLoadingCallback = new HtmlLinkedResourceLoadingCallback();

    // Belgeyi yüklediğimizde, geri aramamız CSS stil sayfaları ve resimler gibi bağlantılı kaynakları işleyecektir.
    Document doc = new Document(MyDir + "Images.html", loadOptions);
    doc.Save(ArtifactsDir + "LoadOptions.LoadOptionsCallback.pdf");
}

/// <summary>
/// Tüm harici stil sayfalarının dosya adlarını yazdırır ve yüklenen bir HTML belgesindeki tüm görselleri bunlarla değiştirir.
/// </summary>
private class HtmlLinkedResourceLoadingCallback : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        switch (args.ResourceType)
        {
            case ResourceType.CssStyleSheet:
                Console.WriteLine($"External CSS Stylesheet found upon loading: {args.OriginalUri}");
                return ResourceLoadingAction.Default;
            case ResourceType.Image:
                Console.WriteLine($"External Image found upon loading: {args.OriginalUri}");

                const string newImageFilename = "Logo.jpg";
                Console.WriteLine($"\tImage will be substituted with: {newImageFilename}");

                Image newImage = Image.FromFile(ImageDir + newImageFilename);

                ImageConverter converter = new ImageConverter();
                byte[] imageBytes = (byte[])converter.ConvertTo(newImage, typeof(byte[]));
                args.SetData(imageBytes);

                return ResourceLoadingAction.UserProvided;
        }

        return ResourceLoadingAction.Default;
    }
}
```

### Ayrıca bakınız

* interface [IResourceLoadingCallback](../../iresourceloadingcallback/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
