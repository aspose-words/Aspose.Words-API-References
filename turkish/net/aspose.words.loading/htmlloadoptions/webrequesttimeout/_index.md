---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: .NET için Aspose.Words
description: HtmlLoadOptions'ın WebRequestTimeout özelliğini keşfedin, optimum web performansı için zaman aşımı ayarlarını özelleştirebilirsiniz. Varsayılan, 100 saniye.
type: docs
weight: 80
url: /tr/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Web isteği zaman aşımına uğramadan önce beklenecek milisaniye sayısı. Varsayılan değer 100000 milisaniyedir (100 saniye).

```csharp
public int WebRequestTimeout { get; set; }
```

## Notlar

HTML ve MHTML belgelerine bağlı harici kaynakları (görüntüler, style sayfaları) yüklerken Aspose.Words'ün yanıt beklediği milisaniye sayısı.

## Örnekler

URL'lerle bağlantılı harici kaynaklara sahip bir belge yüklenirken web istekleri için bir zaman sınırının nasıl ayarlanacağını gösterir.

```csharp
public void WebRequestTimeout()
{
    // Yeni bir HtmlLoadOptions nesnesi oluşturun ve bir web isteği için zaman aşımı eşiğini doğrulayın.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // Harici olarak bir web adresi URL'si ile bağlantılı kaynaklara sahip bir Html belgesi yüklenirken,
    // Aspose.Words, kaynakları bu zaman sınırı içerisinde getirmeyi başaramayan web isteklerini milisaniyelerle sonlandıracaktır.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Yükleme sırasında oluşan tüm uyarıları kaydedecek bir WarningCallback ayarlayın.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Böyle bir belgeyi yükleyin ve resim verisi içeren bir şeklin oluşturulduğunu doğrulayın.
    // Bu bağlantılı görselin yüklenmesi için bir web isteği gerekecek ve bu isteğin zaman sınırımız içerisinde tamamlanması gerekecek.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Makul olmayan bir zaman aşımı sınırı ayarlayın ve belgeyi tekrar yüklemeyi deneyin.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // Zaman sınırı içerisinde bir görüntü elde edemeyen bir web isteği yine de bir görüntü üretecektir.
    // Ancak, görüntü genellikle eksik görüntüleri belirten kırmızı 'x' olacaktır.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Zaman aşımına uğrayan web isteklerinden gelen uyarıları almak için özel bir geri arama da yapılandırabiliriz.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Bir belge yükleme işlemi sırasında oluşan tüm uyarıları bir Listede depolar.
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
