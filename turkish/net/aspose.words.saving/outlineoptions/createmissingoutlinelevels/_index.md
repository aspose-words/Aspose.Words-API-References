---
title: OutlineOptions.CreateMissingOutlineLevels
second_title: Aspose.Words for .NET API Referansı
description: OutlineOptions mülk. Belge dışa aktarıldığında eksik anahat düzeylerinin oluşturulup oluşturulmayacağını belirleyen bir değer alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Belge dışa aktarıldığında eksik anahat düzeylerinin oluşturulup oluşturulmayacağını belirleyen bir değer alır veya ayarlar.

Bu özellik için varsayılan değer:`YANLIŞ`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

### Örnekler

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

* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../outlineoptions/)
* toplantı [Aspose.Words](../../../)


