---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: .NET için Aspose.Words
description: ResourceSaving olayı için gerekli verileri sağlayarak belge işlemenizi geliştiren Aspose.Words.Saving.ResourceSavingArgs sınıfını keşfedin.
type: docs
weight: 6360
url: /tr/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Şunun için veri sağlar:[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) olay.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

```csharp
public class ResourceSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Şu anda kaydedilmekte olan belge nesnesini alır. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Aspose.Words'ün bir kaynağı kaydettikten sonra akışı açık tutması mı yoksa kapatması mı gerektiğini belirtir. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Kaynağın kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Belgeden kaynak dosyasına başvurmak için kullanılan tekdüzen kaynak tanımlayıcısını (URI) alır veya ayarlar. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Kaynağın kaydedileceği akışı belirtmenize olanak tanır. |

## Notlar

Varsayılan olarak, Aspose.Words bir belgeyi sabit sayfa HTML veya SVG'ye kaydettiğinde, her kaynağı ayrı bir dosya olan 'ye kaydeder. Aspose.Words, belgede bulunan her kaynak için benzersiz dosya adı oluşturmak için belge dosya adını ve benzersiz bir numarayı kullanır.

`ResourceSavingArgs` kaynak dosya adlarının nasıl oluşturulacağını yeniden tanımlamanıza veya kendi akış nesnelerinizi sağlayarak kaynakların dosyalara kaydedilmesini tamamen engellemenize olanak tanır.

Kaynak dosya adlarını oluşturmak için kendi mantığınızı uygulamak üzere kullanın[`ResourceFileName`](./resourcefilename/) mülk.

Kaynakları dosyalar yerine akışlara kaydetmek için şunu kullanın:[`ResourceStream`](./resourcestream/) mülk.

## Örnekler

Bir belgeyi HTML'e dönüştürürken oluşturulan dış kaynakları izlemek için bir geri aramanın nasıl kullanılacağını gösterir.

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
