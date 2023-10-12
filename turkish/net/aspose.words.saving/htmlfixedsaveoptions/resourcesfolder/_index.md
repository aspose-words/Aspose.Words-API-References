---
title: HtmlFixedSaveOptions.ResourcesFolder
second_title: Aspose.Words for .NET API Referansı
description: HtmlFixedSaveOptions mülk. Bir belgeyi Html biçiminde dışa aktarırken kaynakların resimler yazı tipleri css kaydedildiği fiziksel klasörü belirtir. Varsayılanhükümsüz .
type: docs
weight: 140
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/
---
## HtmlFixedSaveOptions.ResourcesFolder property

Bir belgeyi Html biçiminde dışa aktarırken kaynakların (resimler, yazı tipleri, css) kaydedildiği fiziksel klasörü belirtir. Varsayılan:`hükümsüz` .

```csharp
public string ResourcesFolder { get; set; }
```

### Notlar

Yalnızca şu durumlarda etkilidir:[`ExportEmbeddedImages`](../exportembeddedimages/) mülkiyet`YANLIŞ`.

Bir kaydettiğinizde[`Document`](../../../aspose.words/document/) Html formatında Aspose.Words'ün belgeye gömülü all görüntülerini bağımsız dosyalar olarak kaydetmesi gerekir.`ResourcesFolder` görüntülerin nereye kaydedileceğini belirtmenize ve[`ResourcesFolderAlias`](../resourcesfolderalias/) , görüntü URI'lerinin nasıl oluşturulacağını belirtmeye olanak tanır.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntülerini belge dosyasının kaydedildiği klasöre kaydeder. Kullanmak`ResourcesFolder` Bu davranışı geçersiz kılmak için .

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'de görüntülerin kaydedileceği bir klasör yoktur, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, erişilebilir bir klasör belirtmeniz gerekir.`ResourcesFolder` mülk

### Örnekler

Bir belgeyi HTML'ye dönüştürürken oluşturulan dış kaynakların URI'lerini yazdırmak için geri aramanın nasıl kullanılacağını gösterir.

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

    // ResourcesFolderAlias tarafından belirtilen bir klasör ResourcesFolder yerine kaynakları içerecektir.
    // Akışların kaynaklarını klasöre koymadan önce klasörün var olduğundan emin olmalıyız.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Sabit HTML'ye dönüştürülürken içerdiği kaynakların URI'lerini sayar ve yazdırır.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // SaveOptions nesnesinde bir klasör takma adı belirlersek, onu buradan yazdırabileceğiz.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Varsayılan olarak 'ResourceFileUri' yazı tipleri için sistem klasörünü kullanır.
                // Diğer platformlardaki sorunları önlemek için yazı tiplerinin yolunu açıkça belirtmelisiniz.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // "ResourcesFolderAlias" özelliğinde bir klasör belirttiysek,
        // kaynağını o klasöre koymak için her akışı yeniden yönlendirmemiz gerekecek.
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


