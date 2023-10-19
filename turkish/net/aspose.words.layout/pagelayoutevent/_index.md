---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.PageLayoutEvent Sıralama. Sayfa düzeni modeli oluşturma ve oluşturma sırasında ortaya çıkan bir olay kodu C#'da.
type: docs
weight: 3370
url: /tr/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Sayfa düzeni modeli oluşturma ve oluşturma sırasında ortaya çıkan bir olay kodu.

Sayfa düzeni modeli iki adımda oluşturulur. İlki, "dönüştürme adımı", bu, sayfa düzeninin belge içeriğini çekip nesne grafiğini oluşturduğu zamandır. İkincisi, "yeniden akıtma adımı", yapıların bölündüğü, birleştirildiği ve düzenlendiği zamandır. sayfalara bölünür.

Oluşturmayı tetikleyen işleme bağlı olarak, sayfa düzeni modeli sabit sayfa formatına dönüştürülebilir veya getirilmeyebilir. Örneğin, belgedeki sayfa sayısını hesaplamak veya alanları güncellemek, oluşturmayı gerektirmezken, Pdf'e aktarma gerektirir.

```csharp
public enum PageLayoutEvent
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan değer |
| WatchDog | `1` | Kodda sıklıkla ziyaret edilen ve işlemi iptal etmeye uygun bir kontrol noktasına karşılık gelir. |
| BuildStarted | `2` | Sayfa düzeninin oluşturulması başladı. Bir kez tetiklendi. Bu, şu durumlarda meydana gelen ilk olaydır:[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) denir. |
| BuildFinished | `3` | Sayfa düzeninin oluşturulması tamamlandı. Bir kez tetiklendi. Bu, şu durumlarda meydana gelen son olaydır:[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) denir. |
| ConversionStarted | `4` | Doküman modelinin sayfa düzenine dönüştürülmesi başladı. Bir kez tetiklendi. Bu, düzen modeli belge içeriğini çekmeye başladığında meydana gelir. |
| ConversionFinished | `5` | Belge modelinin sayfa düzenine dönüştürülmesi tamamlandı. Bir kez tetiklendi. Bu, düzen modeli belge içeriğini çekmeyi bıraktığında meydana gelir. |
| ReflowStarted | `6` | Sayfa düzeninin yeniden düzenlenmesi başladı. Bir kez tetiklendi. Bu, düzen modeli belge içeriğini yeniden akıtmaya başladığında meydana gelir. |
| ReflowFinished | `7` | Sayfa düzeninin yeniden düzenlenmesi tamamlandı. Bir kez tetiklendi. Bu, düzen modeli belge içeriğinin yeniden akışını durdurduğunda meydana gelir. |
| PartReflowStarted | `8` | Sayfanın yeniden akışı başladı. Sayfanın birden çok kez yeniden akıtılabileceğini ve yeniden akışın bitmeden yeniden başlayabileceğini unutmayın. |
| PartReflowFinished | `9` | Sayfanın yeniden akışı tamamlandı. Sayfanın birden çok kez yeniden akıtılabileceğini ve yeniden akışın bitmeden yeniden başlayabileceğini unutmayın. |
| PartRenderingStarted | `10` | Sayfanın oluşturulması başladı. Bu, sayfa başına bir kez tetiklenir. |
| PartRenderingFinished | `11` | Sayfanın oluşturulması tamamlandı. Bu, sayfa başına bir kez tetiklenir. |

## Örnekler

Düzen geri çağrısıyla düzen değişikliklerinin nasıl izleneceğini gösterir.

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
/// Belgeyi sabit sayfa formatında kaydettiğimizde bizi bilgilendirir
/// ve yerel dosya sistemindeki bir görüntüye sayfa yeniden akışı gerçekleştirdiğimiz bir sayfayı işler.
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
