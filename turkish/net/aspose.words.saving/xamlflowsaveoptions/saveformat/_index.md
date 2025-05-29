---
title: XamlFlowSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Belgelerinizi XamlFlow formatında kolayca kaydetmek için XamlFlowSaveOptions SaveFormat özelliğini keşfedin. Bu temel özellik ile iş akışınızı optimize edin!
type: docs
weight: 60
url: /tr/net/aspose.words.saving/xamlflowsaveoptions/saveformat/
---
## XamlFlowSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaXamlFlow .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Örnekler

Bir belgenin akış biçimindeki .xaml'e dönüştürülmesi sırasında oluşturulan bağlantılı resimlerin dosya adlarının nasıl yazdırılacağını gösterir.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "XamlFlowSaveOptions" nesnesi oluşturun
    // Belgeyi XAML kaydetme biçimine nasıl kaydedeceğimizi değiştirmek için.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Yerel dosya sistemindeki bir klasörü atamak için "ImagesFolder" özelliğini kullanın.
    // Aspose.Words belgenin tüm bağlantılı resimlerini kaydedecektir.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Bu klasörü kullanmak için "ImagesFolderAlias" özelliğini kullanın
    // images klasörünün adı yerine image URI'leri oluşturulurken.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // "ImagesFolderAlias" ile belirtilen bir klasörün "ImagesFolder" yerine kaynakları içermesi gerekecektir.
    // Geri arama akışlarının kaynaklarını içine koyabilmesi için klasörün var olduğundan emin olmalıyız.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Üst belgeleri akış biçimindeki .xaml'e dönüştürülürken resimlerin dosya adlarını sayar ve yazdırır.
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

        // Bir resim klasörü takma adı belirtseydik, ayrıca şuna da ihtiyacımız olurdu:
        // her akışı, görüntüsünü alias klasörüne koyacak şekilde yönlendirmek için.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XamlFlowSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
