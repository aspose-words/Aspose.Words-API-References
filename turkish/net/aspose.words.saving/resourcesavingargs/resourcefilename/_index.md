---
title: ResourceSavingArgs.ResourceFileName
second_title: Aspose.Words for .NET API Referansı
description: ResourceSavingArgs mülk. Kaynağın kaydedileceği dosya adını yol olmadan alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

Kaynağın kaydedileceği dosya adını (yol olmadan) alır veya ayarlar.

```csharp
public string ResourceFileName { get; set; }
```

### Notlar

Bu özellik, sabit sayfa HTML'sine veya SVG'ye dışa aktarma sırasında kaynak dosya adlarının nasıl oluşturulduğunu yeniden tanımlamanıza olanak tanır.

Etkinlik başlatıldığında bu özellik, Aspose.Words tarafından oluşturulan dosya adını içerir. Kaynağı farklı bir dosyaya kaydetmek için bu özelliğin değerini değiştirebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, sabit sayfa HTML'sine veya SVG formatına aktarırken her kaynak için otomatik olarak benzersiz bir dosya adı oluşturur. Kaynak dosya adının nasıl oluşturulduğu ( ), belgeyi bir dosyaya mı yoksa bir akışa mı kaydettiğinize bağlıdır.

Bir belgeyi bir dosyaya kaydederken oluşturulan kaynak dosya adı gibi görünür&lt;belge tabanı dosya adı&gt;.&lt;görüntü numarası&gt;.&lt;uzantı&gt;.

Bir belgeyi bir akışa kaydederken oluşturulan kaynak dosya adı gibi görünürAspose.Words.&lt;belge kılavuzu&gt;.&lt;görüntü numarası&gt;.&lt;uzantı&gt;.

`ResourceFileName` yol olmadan yalnızca dosya adını içermelidir. Aspose.Words, kaydetme yolunu ve dosyanın değerini belirler.`kaynak` belge dosya adını kullanarak sabit sayfa HTML'sine veya SVG'ye yazma özelliği,[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) veya[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) Ve[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) veya[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) özellikler.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

### Örnekler

Bir belgeyi HTML'ye dönüştürürken oluşturulan harici kaynakları izlemek için geri aramanın nasıl kullanılacağını gösterir.

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
    /// Aspose.Words harici bir kaynağı sabit sayfa HTML'sine veya SVG'ye kaydettiğinde çağrılır.
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


