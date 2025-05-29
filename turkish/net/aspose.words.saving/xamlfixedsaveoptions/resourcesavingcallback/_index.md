---
title: XamlFixedSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: .NET için Aspose.Words
description: XamlFixedSaveOptions ResourceSavingCallback ile belge dışa aktarımlarınızı optimize edin. Gelişmiş XAML format verimliliği için görüntü ve yazı tipi kaydetmeyi kontrol edin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/
---
## XamlFixedSaveOptions.ResourceSavingCallback property

Bir belge sabit sayfa Xaml biçimine aktarıldığında kaynakların (görüntüler ve yazı tipleri) nasıl kaydedileceğini kontrol etmenizi sağlar.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

## Örnekler

Bir belgeyi sabit biçimli .xaml'e dönüştürürken oluşturulan bağlantılı kaynakların URI'lerinin nasıl yazdırılacağını gösterir.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "XamlFixedSaveOptions" nesnesi oluşturun
    // Belgeyi XAML kaydetme biçimine nasıl kaydedeceğimizi değiştirmek için.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Yerel dosya sisteminde bir klasör atamak için "ResourcesFolder" özelliğini kullanın.
    // Aspose.Words, belgenin tüm bağlantılı kaynaklarını (resimler ve yazı tipleri gibi) kaydedecektir.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Bu klasörü kullanmak için "ResourcesFolderAlias" özelliğini kullanın
    // kaynaklar klasörünün adı yerine görüntü URI'leri oluşturulurken.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // "ResourcesFolderAlias" ile belirtilen bir klasörün "ResourcesFolder" yerine kaynakları içermesi gerekir.
    // Geri arama akışlarının kaynaklarını içine koyabilmesi için klasörün var olduğundan emin olmalıyız.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Sabit .xaml'e dönüştürme sırasında oluşturulan kaynakların URI'lerini sayar ve yazdırır.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // Bir kaynak klasörü takma adı belirtseydik, ayrıca şuna da ihtiyacımız olurdu:
        // her akışı, kaynağını takma ad klasörüne koymak üzere yönlendirmek için.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Ayrıca bakınız

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [XamlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
