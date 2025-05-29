---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: .NET için Aspose.Words
description: PDF ana hatlarınızı zahmetsizce özelleştirmek için PdfSaveOptions' OutlineOptions özelliğini keşfedin. Gezinmeyi geliştirin ve belge kullanılabilirliğini iyileştirin!
type: docs
weight: 240
url: /tr/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Anahat seçeneklerini belirtmenize olanak tanır.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Notlar

Başlıklardan ve yer imlerinden ana hatlar oluşturulabilir.

Başlıklar için anahat düzeyi başlık düzeyine göre belirlenir.

Ana hatlara dahil edilecek maksimum başlık seviyesini ayarlamak veya başlık ana hatlarını tamamen devre dışı bırakmak mümkündür.

Yer imleri için anahat düzeyi, tüm yer imleri için varsayılan değer olarak veya belirli yer imleri için ayrı değerler olarak seçeneklerde ayarlanabilir.

Ayrıca, aynı şekilde ana hatlar XPS formatına aktarılabilir`OutlineOptions` sınıf.

## Örnekler

Kaydedilen bir PDF belgesinin ana hatlarında görünecek başlık düzeyinin nasıl sınırlandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 1, 2 ve sonra 3. düzeylerde İçindekiler girişi olarak kullanılabilecek başlıklar ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içerik tablosu olan bir ana hat içerecektir.
// Bu taslaktaki bir girdiye tıkladığımızda ilgili başlığın bulunduğu yere gideceğiz.
// Anahattan 2'nin üstündeki tüm başlıkları hariç tutmak için "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayın.
// Yukarıda eklediğimiz son iki başlık görünmeyecektir.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

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

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
