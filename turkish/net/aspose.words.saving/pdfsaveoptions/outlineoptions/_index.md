---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words for .NET
description: PdfSaveOptions OutlineOptions mülk. Anahat seçeneklerini belirlemeye izin verir C#'da.
type: docs
weight: 240
url: /tr/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Anahat seçeneklerini belirlemeye izin verir.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Notlar

Ana hatlar başlıklardan ve yer imlerinden oluşturulabilir.

Başlıklar için anahat düzeyi başlık düzeyine göre belirlenir.

Ana hatlara dahil edilecek maksimum başlık düzeyini ayarlamak veya başlık ana hatlarını tamamen devre dışı bırakmak mümkündür.

Yer imleri için anahat düzeyi, seçeneklerde tüm yer imleri için varsayılan değer olarak veya belirli yer imleri için ayrı değerler olarak ayarlanabilir.

Ayrıca ana hatlar aynı kullanılarak XPS formatına aktarılabilir.`OutlineOptions` sınıf.

## Örnekler

Kaydedilmiş bir PDF belgesinin ana hatlarında görünecek başlık düzeyinin nasıl sınırlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Seviye 1, 2 ve ardından 3'ün İçindekiler girişi olarak kullanılabilecek başlıklar ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir taslak içerecektir.
// Bu taslaktaki bir girişe tıklamak bizi ilgili başlığın konumuna götürecektir.
// Seviyeleri 2'nin üzerinde olan tüm başlıkları anahattan hariç tutmak için "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayın.
// Yukarıda eklediğimiz son iki başlık görünmeyecek.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

Bir PDF belgesini kaydederken karşılık gelen başlıklar içermeyen anahat düzeyleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Seviye 1 ve 5'in İçindekiler girişi olarak kullanılabilecek başlıkları ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir taslak içerecektir.
// Bu taslaktaki bir girişe tıklamak bizi ilgili başlığın konumuna götürecektir.
// 5. düzey ve altındaki tüm başlıkları ana hatta dahil etmek için "HeadingsOutlineLevels" özelliğini "5" olarak ayarlayın.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Bu belge 1 ve 5. seviye başlıklarını içerir, 2, 3 ve 4. seviye başlıklarını içermez.
// Çıktı PDF belgesi, 2, 3 ve 4. taslak düzeylerini "eksik" olarak değerlendirecektir.
// Tüm eksik seviyeleri ana hatta dahil etmek için "CreateMissingOutlineLevels" özelliğini "true" olarak ayarlayın,
// kullanılabilir başlık olmadığından boş taslak girişleri bırakıyoruz.
// Eksik anahat seviyelerini yok saymak için "CreateMissingOutlineLevels" özelliğini "false" olarak ayarlayın,
// ve anahat düzeyi 5 başlıklarını düzey 2 olarak değerlendirin.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Ayrıca bakınız

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
