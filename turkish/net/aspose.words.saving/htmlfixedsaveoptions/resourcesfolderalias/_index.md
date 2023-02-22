---
title: HtmlFixedSaveOptions.ResourcesFolderAlias
second_title: Aspose.Words for .NET API Referansı
description: HtmlFixedSaveOptions mülk. Bir Html belgesine yazılan görüntü URIlerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılanhükümsüz .
type: docs
weight: 150
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/
---
## HtmlFixedSaveOptions.ResourcesFolderAlias property

Bir Html belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan`hükümsüz` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

### Notlar

Bir kaydettiğinizde[`Document`](../../../aspose.words/document/) Html formatında Aspose.Words'ün belgeye gömülü all resimleri bağımsız dosyalar olarak kaydetmesi gerekir.[`ResourcesFolder`](../resourcesfolder/) , görüntülerin nereye kaydedileceğini belirlemenize ve`ResourcesFolderAlias` , görüntü URI'lerinin nasıl oluşturulacağını belirlemeye izin verir.

### Örnekler

Bir belgeyi HTML'ye dönüştürürken oluşturulan harici kaynakların URI'lerini yazdırmak için bir geri aramanın nasıl kullanılacağını gösterir.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // ResourcesFolderAlias tarafından belirtilen bir klasör, ResourcesFolder yerine kaynakları içerecektir.
    // Akışlar kaynaklarını içine koymadan önce klasörün var olduğundan emin olmalıyız.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Sabit HTML'ye dönüştürüldükçe içerdiği kaynakların URI'lerini sayar ve yazdırır.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // SaveOptions nesnesinde bir klasör takma adı belirlersek, buradan yazdırabiliriz.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Varsayılan olarak, 'ResourceFileUri' yazı tipleri için sistem klasörünü kullanır.
                // Diğer platformlarda sorun yaşamamak için yazı tiplerinin yolunu açıkça belirtmelisiniz.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // "ResourcesFolderAlias" özelliğinde bir klasör belirlediysek,
        // Kaynağını o klasöre koymak için her akışı yeniden yönlendirmemiz gerekecek.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* toplantı [Aspose.Words](../../../)


