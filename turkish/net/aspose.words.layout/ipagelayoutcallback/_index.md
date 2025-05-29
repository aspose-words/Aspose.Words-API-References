---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: .NET için Aspose.Words
description: Aspose.Words.Layout.IPageLayoutCallback arayüzü ile belge düzeninizi özelleştirin. En iyi sonuçlar için kendi yöntemlerinizle işlemeyi geliştirin.
type: docs
weight: 3760
url: /tr/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Sayfa düzeni modelinin oluşturulması ve işlenmesi sırasında kendi özel yönteminizin çağrılmasını istiyorsanız bu arayüzü uygulayın.

```csharp
public interface IPageLayoutCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | Bu, düzen oluşturma ve işleme ilerlemesini bildirmek için çağrılır. |

## Notlar

Bu arayüzün birincil kullanımı uygulama kodunun derleme sürecini iptal etmesine izin vermektir.

Belgenin başında yalnızca birkaç sayfa için sayfa düzeni modeli oluşturmak ve ardından işlemi iptal edip yalnızca daha önce oluşturulmuş olanları işlemek mümkündür.

Ancak, işlem tamamlanmış olsaydı her sayfa için oluşturulacak olan sonuçların, oluşturma sonuçlarıyla uyuşmayabileceğini unutmayın.

Bu teknik her belge için işe yaramayabilir veya tamamen başarısız olabilir.

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

* property [Callback](../layoutoptions/callback/)
* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
