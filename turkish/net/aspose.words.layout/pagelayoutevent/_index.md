---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: .NET için Aspose.Words
description: Belge oluşturma ve oluşturma sırasında sayfa düzeni olaylarını optimize etmek için gerekli olan Aspose.Words.Layout.PageLayoutEvent enum'unu keşfedin. İş akışınızı bugün geliştirin!
type: docs
weight: 3820
url: /tr/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Sayfa düzeni modelinin oluşturulması ve işlenmesi sırasında ortaya çıkan bir olay kodu.

Sayfa düzeni modeli iki adımda oluşturulur. Birincisi, "dönüşüm adımı", bu, sayfa düzeninin belge içeriğini çekip nesne grafiğini oluşturduğu adımdır. İkincisi, "yeniden akış adımı", bu, yapıların bölündüğü, birleştirildiği ve sayfalara yerleştirildiği adımdır.

Oluşturmayı tetikleyen işleme bağlı olarak, sayfa düzeni modeli sabit sayfa biçimine daha fazla işlenebilir veya işlenmeyebilir. Örneğin, belgedeki sayfa sayısının hesaplanması veya alanların güncellenmesi işleme gerektirmezken, PDF'e aktarma gerektirir.

```csharp
public enum PageLayoutEvent
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan değer |
| WatchDog | `1` | Kodda sıkça ziyaret edilen ve işlemi sonlandırmaya uygun bir kontrol noktasına karşılık gelir. |
| BuildStarted | `2` | Sayfa düzeninin oluşturulması başladı. Bir kez tetiklendi. Bu, şu anda meydana gelen ilk olaydır:[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) denir. |
| BuildFinished | `3` | Sayfa düzeninin oluşturulması tamamlandı. Bir kez tetiklendi. Bu, şu anda meydana gelen son olaydır:[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) denir. |
| ConversionStarted | `4` | Belge modelinin sayfa düzenine dönüştürülmesi başladı. Bir kez tetiklendi. Bu, düzen modelinin belge içeriğini çekmeye başlamasıyla gerçekleşir. |
| ConversionFinished | `5` | Belge modelinin sayfa düzenine dönüştürülmesi tamamlandı. Bir kez tetiklendi. Bu, düzen modelinin belge içeriğini çekmeyi bırakmasıyla oluşur. |
| ReflowStarted | `6` | Sayfa düzeninin yeniden akışı başladı. Bir kez tetiklendi. Bu, düzen modeli belge içeriğini yeniden akıtmaya başladığında gerçekleşir. |
| ReflowFinished | `7` | Sayfa düzeninin yeniden akışı tamamlandı. Bir kez tetiklendi. Bu, düzen modelinin belge içeriğini yeniden akışını durdurduğu zaman meydana gelir. |
| PartReflowStarted | `8` | Sayfanın yeniden akışı başladı. Sayfanın birden fazla kez yeniden akabileceğini ve yeniden akışın bitmeden önce yeniden başlayabileceğini unutmayın. |
| PartReflowFinished | `9` | Sayfanın yeniden akışı tamamlandı. Sayfanın birden fazla kez yeniden akabileceğini ve yeniden akışın tamamlanmadan önce yeniden başlatılabileceğini unutmayın. |
| PartRenderingStarted | `10` | Sayfanın işlenmesi başladı. Bu, sayfa başına bir kez tetiklenir. |
| PartRenderingFinished | `11` | Sayfanın işlenmesi tamamlandı. Bu, sayfa başına bir kez tetiklenir. |

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

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
