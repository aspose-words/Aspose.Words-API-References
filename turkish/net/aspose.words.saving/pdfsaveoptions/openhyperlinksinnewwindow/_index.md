---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: .NET için Aspose.Words
description: PDF'nizdeki köprü metni davranışını PdfSaveOptions ile kontrol edin. Gelişmiş kullanıcı deneyimi için bağlantıları yeni bir pencerede veya sekmede açılacak şekilde kolayca ayarlayın.
type: docs
weight: 230
url: /tr/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Çıktı Pdf belgesindeki köprü metinlerinin bir tarayıcının yeni bir penceresinde (veya sekmesinde) açılmasının zorunlu olup olmadığını belirleyen bir değer alır veya ayarlar.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` Bu değer olarak ayarlandığında`doğru` köprü metinleri JavaScript kodu kullanılarak kaydedilir. JavaScript kodu`app.launchURL("URL", doğru);` , nerede`URL` bir köprü metnidir.

Bu seçeneğin şu şekilde ayarlandığını unutmayın:`doğru` hiperlinkler bazı PDF okuyucularında (örneğin Chrome, Firefox) çalışamaz

PDF/A-1 ve PDF/A-2 uyumluluğu JavaScript eylemlerini yasaklamaktadır.`YANLIŞ`PDF/A-1 ve PDF/A-2'ye kayıt yaparken otomatik olarak kullanılacaktır.

## Örnekler

PDF'e dönüştürdüğümüz bir belgedeki köprü metinlerinin, üzerine tıkladığımızda yeni sayfalar açacak şekilde nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", yanlış);

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Javascript kodunu kullanarak tüm köprü metinlerini kaydetmek için "OpenHyperlinksInNewWindow" özelliğini "true" olarak ayarlayın
// okuyucuların bu bağlantıları yeni pencerelerde/tarayıcı sekmelerinde açmasını zorunlu kılar.
// Tüm köprü metinlerini normal şekilde kaydetmek için "OpenHyperlinksInNewWindow" özelliğini "false" olarak ayarlayın.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
