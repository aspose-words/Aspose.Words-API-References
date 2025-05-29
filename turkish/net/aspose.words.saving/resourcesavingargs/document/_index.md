---
title: ResourceSavingArgs.Document
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: Kaydedilen geçerli belge nesnesine erişmek için ResourceSavingArgs Belge özelliğini keşfedin; böylece iş akışınızın verimliliğini artırın.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/resourcesavingargs/document/
---
## ResourceSavingArgs.Document property

Şu anda kaydedilmekte olan belge nesnesini alır.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [ResourceSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
