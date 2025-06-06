---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: .NET için Aspose.Words
description: Belgelerinizdeki kaynak dosyalarını kolayca yönetmek ve başvurmak için ResourceSavingArgs ResourceFileUri özelliğini keşfedin. Verimliliği bugün artırın!
type: docs
weight: 40
url: /tr/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Belgeden kaynak dosyasına başvurmak için kullanılan tekdüzen kaynak tanımlayıcısını (URI) alır veya ayarlar.

```csharp
public string ResourceFileUri { get; set; }
```

## Notlar

Bu özellik, sabit sayfa HTML veya SVG belgelerine aktarılan kaynak dosyalarının URI'lerini değiştirmenize olanak tanır.

Aspose.Words, sabit sayfa HTML veya SVG biçimine aktarma sırasında her kaynak dosyası için otomatik olarak bir URI oluşturur. Oluşturulan URI'ler Aspose.Words tarafından kaydedilen kaynak dosyalarına başvurur. Ancak, kaynak dosyaları başka bir yere taşınacaksa veya kaynak dosyaları akışlara kaydedilirse URI'ler yanlış olabilir. Bu özellik, bu durumlarda URI'leri düzeltmeye olanak tanır.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından olarak oluşturulan URI'yi içerir. Kaynak dosyası için özel bir URI sağlamak üzere bu özelliğin değerini değiştirebilirsiniz.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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

* class [ResourceSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
