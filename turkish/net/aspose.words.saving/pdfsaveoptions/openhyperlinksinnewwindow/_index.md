---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Pdf Document çıktısındaki köprülerin bir tarayıcının yeni bir penceresinde veya sekmesinde açılmaya zorlanıp zorlanmadığını belirleyen bir değer alır veya ayarlar.
type: docs
weight: 200
url: /tr/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Pdf Document çıktısındaki köprülerin bir tarayıcının yeni bir penceresinde (veya sekmesinde) açılmaya zorlanıp zorlanmadığını belirleyen bir değer alır veya ayarlar.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

### Notlar

Varsayılan değer`yanlış` . Bu değer olarak ayarlandığında`doğru` köprüler JavaScript kodu kullanılarak kaydedilir. JavaScript kodu`app.launchURL("URL", doğru);`, nerede`URL` bir köprüdür.

Bu seçeneğin`doğru` köprüler, Chrome, Firefox gibi bazı PDF okuyucularında çalışamaz.

JavaScript eylemleri, PDF/A-1 ve PDF/A-2 uyumluluğu tarafından yasaklanmıştır.`yanlış` PDF/A-1 ve PDF/A-2'ye kaydedildiğinde otomatik olarak kullanılacaktır.

### Örnekler

PDF'ye dönüştürdüğümüz bir belgede köprülerin nasıl kaydedileceğini gösterir, böylece üzerlerine tıkladığımızda yeni sayfalar açarlar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Javascript kodunu kullanarak tüm köprüleri kaydetmek için "OpenHyperlinksInNewWindow" özelliğini "true" olarak ayarlayın
// okuyucuları bu bağlantıları yeni pencerelerde/tarayıcı sekmelerinde açmaya zorlar.
// Tüm köprüleri normal şekilde kaydetmek için "OpenHyperlinksInNewWindow" özelliğini "false" olarak ayarlayın.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


