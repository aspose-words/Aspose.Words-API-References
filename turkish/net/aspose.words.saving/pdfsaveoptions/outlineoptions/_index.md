---
title: PdfSaveOptions.OutlineOptions
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Anahat seçeneklerini belirlemeye izin verir.
type: docs
weight: 210
url: /tr/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Anahat seçeneklerini belirlemeye izin verir.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Notlar

Ana hatlar, başlıklardan ve yer imlerinden oluşturulabilir.

Başlıklar için anahat düzeyi başlık düzeyine göre belirlenir.

Ana hatlara dahil edilecek maksimum başlık seviyesini ayarlamak veya başlık ana hatlarını tamamen devre dışı bırakmak mümkündür.

Yer imleri için anahat düzeyi, seçeneklerde tüm yer imleri için varsayılan bir değer olarak veya belirli yer imleri için ayrı değerler olarak ayarlanabilir.

Ayrıca, ana hatlar aynı kullanılarak XPS formatına aktarılabilir.`OutlineOptions` sınıf.

### Örnekler

Kaydedilmiş bir PDF belgesinin ana hatlarında görünecek başlıkların düzeyinin nasıl sınırlandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Seviye 1, 2 ve ardından 3 TOC girişleri olarak hizmet edebilecek başlıklar ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir anahat içerecektir.
// Bu taslakta bir girdiye tıklamak bizi ilgili başlığın konumuna götürecektir.
// Seviyeleri 2'nin üzerinde olan tüm başlıkları anahattan çıkarmak için "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayın.
// Yukarıda eklediğimiz son iki başlık görünmeyecektir.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

Bir PDF belgesini kaydederken karşılık gelen herhangi bir başlık içermeyen anahat düzeyleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Seviye 1 ve 5'in İçindekiler girişi olarak hizmet edebilecek başlıklar ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir anahat içerecektir.
// Bu taslakta bir girdiye tıklamak bizi ilgili başlığın konumuna götürecektir.
// Seviye 5 ve altındaki tüm başlıkları anahatta dahil etmek için "HeadingsOutlineLevels" özelliğini "5" olarak ayarlayın.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

 // Bu belge 1. ve 5. düzey başlıklar içerir ve 2., 3. ve 4. düzey başlıklar içermez.
// Çıktı PDF belgesi, 2, 3 ve 4 anahat düzeylerini "eksik" olarak değerlendirecektir.
// Anahatta tüm eksik seviyeleri dahil etmek için "CreateMissingOutlineLevels" özelliğini "true" olarak ayarlayın,
// Kullanılabilir başlık olmadığı için anahat girişlerini boş bırakıyoruz.
// Eksik anahat düzeylerini yok saymak için "CreateMissingOutlineLevels" özelliğini "false" olarak ayarlayın,
// ve anahat seviyesi 5 başlıklarını seviye 2 olarak ele alın.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Ayrıca bakınız

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


