---
title: XamlFlowSaveOptions.ImageSavingCallback
linktitle: ImageSavingCallback
articleTitle: ImageSavingCallback
second_title: Aspose.Words for .NET
description: XamlFlowSaveOptions ImageSavingCallback mülk. Bir belge XAMLye kaydedildiğinde görüntülerin nasıl kaydedileceğini kontrol etmenize izin verir C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/xamlflowsaveoptions/imagesavingcallback/
---
## XamlFlowSaveOptions.ImageSavingCallback property

Bir belge XAML'ye kaydedildiğinde görüntülerin nasıl kaydedileceğini kontrol etmenize izin verir.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

## Örnekler

Bir belgeyi akış formu .xaml'e dönüştürürken oluşturulan bağlantılı görüntülerin dosya adlarının nasıl yazdırılacağını gösterir.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Belgenin "Save" yöntemine aktarabileceğimiz bir "XamlFlowSaveOptions" nesnesi oluşturun
    // belgeyi XAML kaydetme biçimine nasıl kaydedeceğimizi değiştirmek için.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Yerel dosya sisteminde içine bir klasör atamak için "ImagesFolder" özelliğini kullanın.
    // Aspose.Words belgenin tüm bağlantılı görsellerini kaydedecektir.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Bu klasörü kullanmak için "ImagesFolderAlias" özelliğini kullanın
    // resimler klasörünün adı yerine resim URI'lerini oluştururken.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // "ImagesFolderAlias" tarafından belirtilen bir klasörün "ImagesFolder" yerine kaynakları içermesi gerekecektir.
    // Geri çağrının akışlarının kaynaklarını klasöre koymadan önce klasörün var olduğundan emin olmalıyız.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Ana belgeleri flow-form .xaml'e dönüştürülürken görüntülerin dosya adlarını sayar ve yazdırır.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // Bir resim klasörü takma adı belirtirsek ayrıca buna da ihtiyacımız olur.
        // her akışı, görüntüsünü takma ad klasörüne koymak üzere yeniden yönlendirmek için.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Ayrıca bakınız

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [XamlFlowSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
