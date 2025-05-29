---
title: LayoutOptions.Callback
linktitle: Callback
articleTitle: Callback
second_title: .NET için Aspose.Words
description: Gelişmiş sayfa düzeni özelleştirmesi ve iyileştirilmiş kullanıcı deneyimi için IPageLayoutCallback'i kolayca yönetmek üzere LayoutOptions Geri Arama özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.layout/layoutoptions/callback/
---
## LayoutOptions.Callback property

Alır veya ayarlar[`IPageLayoutCallback`](../../ipagelayoutcallback/) sayfa düzeni modeli tarafından kullanılan uygulama.

```csharp
public IPageLayoutCallback Callback { get; set; }
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

* interface [IPageLayoutCallback](../../ipagelayoutcallback/)
* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
