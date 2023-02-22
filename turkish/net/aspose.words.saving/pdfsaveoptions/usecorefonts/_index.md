---
title: PdfSaveOptions.UseCoreFonts
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Arial Times New Roman Courier New ve Symbol TrueType yazı tiplerinin çekirdek PDF Tip 1 yazı tipleriyle değiştirilip değiştirilmeyeceğini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 280
url: /tr/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

Arial, Times New Roman, Courier New ve Symbol TrueType yazı tiplerinin çekirdek PDF Tip 1 yazı tipleriyle değiştirilip değiştirilmeyeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseCoreFonts { get; set; }
```

### Notlar

Varsayılan değer`yanlış` . Bu değer olarak ayarlandığında`doğru` Arial, Times New Roman, Courier New ve Symbol yazı tipleri, PDF belgesinde karşılık gelen temel Tip 1 yazı tipiyle değiştirilir.

Temel PDF yazı tiplerinin veya yazı tipi ölçütlerinin ve uygun ikame yazı tiplerinin herhangi bir PDF görüntüleyici uygulamasında mevcut olması gerekir.

Bu ayar yalnızca ANSI (Windows-1252) kodlamasındaki metin için çalışır. ANSI olmayan metin, bu ayardan bağımsız olarak gömülü TrueType yazı tipiyle yazılacaktır.

PDF/A ve PDF/UA uyumluluğu, tüm yazı tiplerinin gömülü olmasını gerektirir.`yanlış` değer, PDF/A ve PDF/UA'ya kaydederken otomatik olarak kullanılır .

PDF 2.0 biçiminde kaydederken çekirdek yazı tipleri desteklenmez.`yanlış`değer, PDF 2.0'a kaydedilirken otomatik olarak kullanılır .

Bu seçenek daha yüksek önceliğe sahiptir.[`FontEmbeddingMode`](../fontembeddingmode/) seçenek.

### Örnekler

PDF Tip 1 yazı tipi değiştirmenin nasıl etkinleştirildiğini/devre dışı bırakıldığını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Bazı yazı tiplerini değiştirmek için "UseCoreFonts" özelliğini "true" olarak ayarlayın,
// iki yazı tipini PDF Tip 1 eşdeğerleriyle birlikte belgemize dahil ediyoruz.
// PDF Type 1 yazı tiplerini uygulamamak için "UseCoreFonts" özelliğini "false" olarak ayarlayın.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);

if (useCoreFonts)
    Assert.That(3000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
else
    Assert.That(30000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


