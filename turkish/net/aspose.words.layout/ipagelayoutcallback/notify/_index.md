---
title: IPageLayoutCallback.Notify
second_title: Aspose.Words for .NET API Referansı
description: IPageLayoutCallback yöntem. Bu düzen oluşturma ve işleme ilerleme durumunu bildirmek için çağrılır.
type: docs
weight: 10
url: /tr/net/aspose.words.layout/ipagelayoutcallback/notify/
---
## IPageLayoutCallback.Notify method

Bu, düzen oluşturma ve işleme ilerleme durumunu bildirmek için çağrılır.

```csharp
public void Notify(PageLayoutCallbackArgs args)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| args | PageLayoutCallbackArgs | Olayın bir argümanı. |

### Notlar

Uygulama tarafından oluşturulduğunda özel durum, düzen oluşturma işlemini iptal eder.

### Örnekler

Bir düzen geri çağırma ile düzen değişikliklerinin nasıl izleneceğini gösterir.

```csharp
[Test]
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
/// Belgeyi sabit bir sayfa biçiminde kaydettiğimizde bize haber verir
/// ve yerel dosya sistemindeki bir görüntüye sayfa yeniden akışı gerçekleştirdiğimiz bir sayfayı oluşturur.
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

* class [PageLayoutCallbackArgs](../../pagelayoutcallbackargs/)
* interface [IPageLayoutCallback](../)
* ad alanı [Aspose.Words.Layout](../../ipagelayoutcallback/)
* toplantı [Aspose.Words](../../../)


