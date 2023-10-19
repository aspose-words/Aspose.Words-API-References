---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words for .NET
description: PdfSaveOptions OpenHyperlinksInNewWindow mülk. Pdf document çıktısındaki köprülerin tarayıcının yeni bir penceresinde veya sekmesinde açılmaya zorlanıp zorlanmayacağını belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 230
url: /tr/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Pdf document çıktısındaki köprülerin tarayıcının yeni bir penceresinde (veya sekmesinde) açılmaya zorlanıp zorlanmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` . Bu değer şu şekilde ayarlandığında`doğru` köprüler JavaScript kodu kullanılarak kaydedilir. JavaScript kodu`app.launchURL("URL", doğru);` , nerede`URL'si` bir köprüdür.

Bu seçeneğin şu şekilde ayarlandığını unutmayın:`doğru` köprüler Chrome, Firefox gibi bazı PDF okuyucularda çalışamaz .

JavaScript eylemleri PDF/A-1 ve PDF/A-2 uyumluluğu nedeniyle yasaklanmıştır.`YANLIŞ` PDF/A-1 ve PDF/A-2'ye kaydedildiğinde otomatik olarak kullanılacaktır.

## Örnekler

PDF'ye dönüştürdüğümüz bir belgedeki köprülerin, üzerlerine tıkladığımızda yeni sayfalar açmaları için nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Javascript kodunu kullanarak tüm köprüleri kaydetmek için "OpenHyperlinksInNewWindow" özelliğini "true" olarak ayarlayın
// okuyucuları bu bağlantıları yeni pencerelerde/tarayıcı sekmelerinde açmaya zorlar.
// Tüm köprüleri normal şekilde kaydetmek için "OpenHyperlinksInNewWindow" özelliğini "false" olarak ayarlayın.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
