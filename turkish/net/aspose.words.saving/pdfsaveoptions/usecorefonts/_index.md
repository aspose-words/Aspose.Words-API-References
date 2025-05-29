---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: .NET için Aspose.Words
description: PDF'lerinizi PdfSaveOptions ile optimize edin! Belge kalitesini artırmak için Arial ve Times New Roman gibi TrueType yazı tipleri için yazı tipi değiştirmeyi kontrol edin.
type: docs
weight: 330
url: /tr/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

TrueType yazı tipleri Arial, Times New Roman, Courier New ve Symbol'ün çekirdek PDF Type 1 yazı tipleriyle değiştirilip değiştirilmeyeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseCoreFonts { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` Bu değer olarak ayarlandığında`doğru` PDF dokümanında Arial, Times New Roman, Courier New ve Symbol yazı tipleri, karşılık gelen çekirdek Tip 1 yazı tipiyle değiştirildi.

Herhangi bir PDF görüntüleme uygulamasında, temel PDF yazı tipleri veya bunların yazı tipi ölçütleri ve uygun ikame yazı tiplerinin mevcut olması gerekir.

Bu ayar yalnızca ANSI (Windows-1252) kodlamasındaki metin için çalışır. ANSI olmayan metin, bu ayardan bağımsız olarak gömülü TrueType yazı tipiyle yazılacaktır .

PDF/A ve PDF/UA uyumluluğu tüm yazı tiplerinin gömülmesini gerektirir.`YANLIŞ` PDF/A ve PDF/UA'ya kaydederken değer otomatik olarak kullanılacaktır .

PDF 2.0 formatına kaydederken temel yazı tipleri desteklenmiyor.`YANLIŞ` PDF 2.0'a kaydederken değer otomatik olarak kullanılacaktır .

Bu seçeneğin önceliği daha yüksektir[`FontEmbeddingMode`](../fontembeddingmode/) seçenek.

## Örnekler

PDF Type 1 yazı tipi değişiminin nasıl etkinleştirileceğini/devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();
// Bazı yazı tiplerini değiştirmek için "UseCoreFonts" özelliğini "true" olarak ayarlayın.
// belgemizdeki iki yazı tipini, PDF Type 1 eşdeğerleriyle birlikte dahil ediyoruz.
// PDF Type 1 yazı tiplerini uygulamamak için "UseCoreFonts" özelliğini "false" olarak ayarlayın.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
