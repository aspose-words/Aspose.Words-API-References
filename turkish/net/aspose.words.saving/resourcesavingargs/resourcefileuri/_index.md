---
title: ResourceSavingArgs.ResourceFileUri
second_title: Aspose.Words for .NET API Referansı
description: ResourceSavingArgs mülk. Belgeden kaynak dosyasına başvurmak için kullanılan tek tip kaynak tanımlayıcısını URI alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Belgeden kaynak dosyasına başvurmak için kullanılan tek tip kaynak tanımlayıcısını (URI) alır veya ayarlar.

```csharp
public string ResourceFileUri { get; set; }
```

### Notlar

Bu özellik, sabit sayfa HTML veya SVG belgelerine dışa aktarılan kaynak dosyalarının URI'lerini değiştirmenize olanak tanır.

Aspose.Words, sabit sayfa HTML veya SVG formatına dışa aktarma sırasında her kaynak dosyası için otomatik olarak bir URI oluşturur. Oluşturulan URI'ler, Aspose.Words tarafından kaydedilen kaynak dosyalarına başvurur. Ancak, kaynak dosyaları başka bir konuma taşınacaksa veya kaynak dosyaları akışlara kaydedilecekse URI'ler yanlış olabilir. Bu özellik, bu durumlarda URI'lerin düzeltilmesine izin verir.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından tarafından oluşturulan URI'yi içerir. Kaynak dosyası için özel bir URI sağlamak üzere bu özelliğin değerini değiştirebilirsiniz.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

### Örnekler

Bir belgeyi HTML'ye dönüştürürken oluşturulan harici kaynakları izlemek için bir geri aramanın nasıl kullanılacağını gösterir.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// Aspose.Words harici bir kaynağı sabit sayfa HTML veya SVG'ye kaydettiğinde çağrılır.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

### Ayrıca bakınız

* class [ResourceSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../resourcesavingargs/)
* toplantı [Aspose.Words](../../../)


