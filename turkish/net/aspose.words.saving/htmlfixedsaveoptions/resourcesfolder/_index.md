---
title: HtmlFixedSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: .NET için Aspose.Words
description: HtmlFixedSaveOptions ResourcesFolder özelliğinin HTML dışa aktarmaları sırasında resimlerin, yazı tiplerinin ve CSS'nin nerede depolandığını nasıl tanımladığını keşfedin. Belge iş akışınızı optimize edin!
type: docs
weight: 160
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/
---
## HtmlFixedSaveOptions.ResourcesFolder property

Bir belgeyi Html biçimine aktarırken kaynakların (resimler, yazı tipleri, css) kaydedildiği fiziksel klasörü belirtir. Varsayılan`hükümsüz` .

```csharp
public string ResourcesFolder { get; set; }
```

## Notlar

Yalnızca şu durumlarda etkilidir:[`ExportEmbeddedImages`](../exportembeddedimages/) mülkiyet`YANLIŞ`.

Birini kaydettiğinizde[`Document`](../../../aspose.words/document/) Html formatında, Aspose.Words'ün belgeye gömülü tüm resimleri bağımsız dosyalar olarak kaydetmesi gerekir.`ResourcesFolder` görüntülerin nereye kaydedileceğini belirtmenize olanak tanır ve[`ResourcesFolderAlias`](../resourcesfolderalias/) görüntü URI'lerinin nasıl oluşturulacağını belirtmeye izin verir.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak, resimlerini belge dosyasının kaydedildiği klasöre kaydeder.`ResourcesFolder` Bu davranışı geçersiz kılmak için kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'ün görüntüleri kaydedeceği bir klasörü yoktur, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, şu şekilde erişilebilir bir klasör belirtmeniz gerekir: `ResourcesFolder` mülk

## Örnekler

Bir belgeyi HTML'e dönüştürürken oluşturulan harici kaynakların URI'lerini yazdırmak için bir geri aramanın nasıl kullanılacağını gösterir.

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

    // ResourcesFolderAlias tarafından belirtilen klasör ResourcesFolder yerine kaynakları içerecektir.
    // Akışların kaynaklarını koyabilmeleri için klasörün var olduğundan emin olmalıyız.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Sabit HTML'ye dönüştürüldükçe, içerdiği kaynakların URI'lerini sayar ve yazdırır.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // SaveOptions nesnesinde bir klasör takma adı belirlersek buradan yazdırabileceğiz.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Varsayılan olarak, 'ResourceFileUri' yazı tipleri için sistem klasörünü kullanır.
                // Diğer platformlarda sorun yaşamamak için fontların yolunu açıkça belirtmeniz gerekir.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // "ResourcesFolderAlias" özelliğinde bir klasör belirttiysek,
        // ayrıca her akışı, kaynağını o klasöre koyacak şekilde yönlendirmemiz gerekecek.
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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
