---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: .NET için Aspose.Words
description: OutlineOptions'daki CreateMissingOutlineLevels özelliğinin, daha iyi organizasyon için eksik anahat düzeylerini otomatik olarak oluşturarak belge dışa aktarımlarını nasıl geliştirdiğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Belge dışa aktarıldığında eksik anahat düzeylerinin oluşturulup oluşturulmayacağını belirleyen bir değer alır veya ayarlar.

Bu özelliğin varsayılan değeri:`YANLIŞ`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## Örnekler

Bir PDF belgesini kaydederken, karşılık gelen başlıklar içermeyen anahat düzeyleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 1. ve 5. seviye TOC girişleri olarak kullanılabilecek başlıklar ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içerik tablosu olan bir ana hat içerecektir.
// Bu taslaktaki bir girdiye tıkladığımızda ilgili başlığın bulunduğu yere gideceğiz.
// Anahatta 5 ve altındaki tüm düzeylerdeki başlıkların yer alması için "HeadingsOutlineLevels" özelliğini "5" olarak ayarlayın.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Bu belge 1. ve 5. düzey başlıkları içeriyor ve 2., 3. ve 4. düzey başlıkları içermiyor.
// Çıktı PDF belgesi, anahat düzeyleri 2, 3 ve 4'ü "eksik" olarak ele alacaktır.
// Anahattaki tüm eksik seviyeleri dahil etmek için "CreateMissingOutlineLevels" özelliğini "true" olarak ayarlayın,
// Kullanılabilir başlıklar olmadığından boş anahat girişleri bırakılıyor.
// Eksik anahat seviyelerini yok saymak için "CreateMissingOutlineLevels" özelliğini "false" olarak ayarlayın,
// ve 5. seviye anahat başlıklarını 2. seviye olarak ele al.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Ayrıca bakınız

* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
