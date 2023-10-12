---
title: LoadOptions.ResourceLoadingCallback
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. HTML MHTMLden bir belge içe aktarıldığında harici kaynakların resimler stil sayfaları nasıl yükleneceğini kontrol etmeye olanak tanır.
type: docs
weight: 140
url: /tr/net/aspose.words.loading/loadoptions/resourceloadingcallback/
---
## LoadOptions.ResourceLoadingCallback property

HTML, MHTML'den bir belge içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmeye olanak tanır.

```csharp
public IResourceLoadingCallback ResourceLoadingCallback { get; set; }
```

### Örnekler

Html belgeleri yüklenirken harici kaynakların nasıl kullanılacağını gösterir.

```csharp
public void LoadOptionsCallback()
{
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.ResourceLoadingCallback = new HtmlLinkedResourceLoadingCallback();

    // Belgeyi yüklediğimizde geri çağrımız CSS stil sayfaları ve resimler gibi bağlantılı kaynakları yönetecektir.
    Document doc = new Document(MyDir + "Images.html", loadOptions);
    doc.Save(ArtifactsDir + "LoadOptions.LoadOptionsCallback.pdf");
}

/// <summary>
/// Tüm harici stil sayfalarının dosya adlarını yazdırır ve yüklenen bir html belgesinin tüm resimlerini değiştirir.
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
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


