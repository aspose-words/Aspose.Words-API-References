---
title: Class ResourceSavingArgs
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.ResourceSavingArgs sınıf. için veri sağlarResourceSaving olay.
type: docs
weight: 5280
url: /tr/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

için veri sağlar[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) olay.

```csharp
public class ResourceSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Şu anda kaydedilmekte olan belge nesnesini alır. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Aspose.Words'ün bir kaynağı kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Kaynağın kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Belgeden kaynak dosyasına başvurmak için kullanılan tek tip kaynak tanımlayıcısını (URI) alır veya ayarlar. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Kaynağın kaydedileceği akışı belirtmeye izin verir. |

### Notlar

Varsayılan olarak Aspose.Words bir belgeyi sabit sayfa HTML veya SVG'ye kaydettiğinde, her kaynağı ayrı bir dosyasına kaydeder. Aspose.Words, belgede bulunan her kaynak için benzersiz dosya adı oluşturmak için belge dosya adını ve benzersiz bir numarayı kullanır.

`ResourceSavingArgs` kaynak dosya adlarının nasıl oluşturulacağını yeniden tanımlamanıza veya kendi akış nesnelerinizi sağlayarak kaynakların dosyalara kaydedilmesini tamamen engellemenize olanak tanır.

Kaynak dosya adları oluşturmak üzere kendi mantığınızı uygulamak için [`ResourceFileName`](./resourcefilename/) Emlak.

Kaynakları dosyalar yerine akışlara kaydetmek için[`ResourceStream`](./resourcestream/) Emlak.

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


