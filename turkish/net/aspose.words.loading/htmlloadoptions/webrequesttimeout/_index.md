---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words for .NET
description: HtmlLoadOptions WebRequestTimeout mülk. Web isteği zaman aşımına uğramadan önce beklenecek milisaniye sayısı. Varsayılan değer 100000 milliseconds 100 saniye. dir C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Web isteği zaman aşımına uğramadan önce beklenecek milisaniye sayısı. Varsayılan değer 100000 milliseconds (100 saniye). 'dir.

```csharp
public int WebRequestTimeout { get; set; }
```

## Notlar

HTML ve MHTML belgelerine bağlı harici kaynakları (resimler, style sayfalar) yüklerken Aspose.Words'ün yanıt için bekleyeceği milisaniye sayısı.

## Örnekler

URL'lerle bağlanan harici kaynaklara sahip bir belge yüklenirken web istekleri için zaman sınırının nasıl ayarlanacağını gösterir.

```csharp
public void WebRequestTimeout()
{
    // Yeni bir HtmlLoadOptions nesnesi oluşturun ve bir web isteği için zaman aşımı eşiğini doğrulayın.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // Bir web adresi URL'si ile harici olarak bağlanan kaynaklara sahip bir Html belgesi yüklenirken,
    // Aspose.Words, kaynakları bu süre sınırı içinde (milisaniye cinsinden) getiremeyen web isteklerini iptal edecektir.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Yükleme sırasında meydana gelen tüm uyarıları kaydedecek bir WarningCallback ayarlayın.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Böyle bir belge yükleyin ve görüntü verileri içeren bir şeklin oluşturulduğunu doğrulayın.
    // Bu bağlantılı görselin yüklenmesi için bir web isteği gerekecek ve bunun bizim zaman sınırımız içinde tamamlanması gerekecek.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Makul olmayan bir zaman aşımı sınırı belirleyin ve belgeyi yeniden yüklemeyi deneyin.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // Zaman sınırı içinde görüntü elde edemeyen bir web isteği yine de görüntü üretecektir.
    // Ancak resim, genellikle eksik resimleri belirten kırmızı 'x' olacaktır.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Zaman aşımına uğramış web isteklerinden gelen uyarıları almak için özel bir geri arama da yapılandırabiliriz.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Bir belge yükleme işlemi sırasında oluşan tüm uyarıları bir Listede saklar.
/// </summary>
private class ListDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        mWarnings.Add(info);
    }

    public List<WarningInfo> Warnings() { 
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Ayrıca bakınız

* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
