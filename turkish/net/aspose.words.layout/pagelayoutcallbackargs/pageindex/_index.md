---
title: PageLayoutCallbackArgs.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: .NET için Aspose.Words
description: İlgili belge sayfasının 0 tabanlı dizinini sağlayan PageLayoutCallbackArgs'ın PageIndex özelliğini keşfedin. Doğru sayfa izleme ve yeniden akış içgörüleri edinin!
type: docs
weight: 30
url: /tr/net/aspose.words.layout/pagelayoutcallbackargs/pageindex/
---
## PageLayoutCallbackArgs.PageIndex property

Bu olayın ilişkili olduğu belgedeki sayfanın 0 tabanlı dizinini alır. İlişkili bir sayfa yoksa veya sayfa yeniden akış sırasında kaldırılmışsa negatif değer döndürür.

```csharp
public int PageIndex { get; }
```

## Örnekler

Düzen değişikliklerinin düzen geri aramasıyla nasıl izleneceğini gösterir.

```csharp
public void PageLayoutCallback()
{
    Document doc = new Document();
    doc.BuiltInDocumentProperties.Title = "My Document";

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");

    doc.LayoutOptions.Callback = new RenderPageLayoutCallback();
    doc.UpdatePageLayout();

    doc.Save(ArtifactsDir + "Layout.PageLayoutCallback.pdf");
}

/// <summary>
/// Belgeyi sabit bir sayfa biçimine kaydettiğimizde bize bildirir
/// ve yerel dosya sistemindeki bir görüntüye sayfa yeniden akışı gerçekleştirdiğimiz bir sayfa oluşturur.
/// </summary>
private class RenderPageLayoutCallback : IPageLayoutCallback
{
    public void Notify(PageLayoutCallbackArgs a)
    {
        switch (a.Event)
        {
            case PageLayoutEvent.PartReflowFinished:
                NotifyPartFinished(a);
                break;
            case PageLayoutEvent.ConversionFinished:
                NotifyConversionFinished(a);
                break;
        }
    }

    private void NotifyPartFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Part at page {a.PageIndex + 1} reflow.");
        RenderPage(a, a.PageIndex);
    }

    private void NotifyConversionFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Document \"{a.Document.BuiltInDocumentProperties.Title}\" converted to page format.");
    }

    private void RenderPage(PageLayoutCallbackArgs a, int pageIndex)
    {
        ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png) { PageSet = new PageSet(pageIndex) };

        using (FileStream stream =
            new FileStream(ArtifactsDir + $@"PageLayoutCallback.page-{pageIndex + 1} {++mNum}.png",
                FileMode.Create))
            a.Document.Save(stream, saveOptions);
    }

    private int mNum;
}
```

### Ayrıca bakınız

* class [PageLayoutCallbackArgs](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
