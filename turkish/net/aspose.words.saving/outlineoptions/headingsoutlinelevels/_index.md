---
title: OutlineOptions.HeadingsOutlineLevels
second_title: Aspose.Words for .NET API Referansı
description: OutlineOptions mülk. belge taslağına kaç düzeyde başlık Başlık stilleriyle biçimlendirilmiş paragraflar ekleneceğini belirtir.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

belge taslağına kaç düzeyde başlık (Başlık stilleriyle biçimlendirilmiş paragraflar) ekleneceğini belirtir.

```csharp
public int HeadingsOutlineLevels { get; set; }
```

### Notlar

Anahatta başlık olmaması durumunda 0 belirtin; Anahattaki başlıkların bir düzeyi için 1'i belirtin ve bu şekilde devam edin.

Varsayılan 0'dır. Geçerli aralık 0 ila 9'dur.

### Örnekler

Belgenin ana hatlarında üç düzeyde bir belgenin tamamının PDF'ye nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 1'den 5'e kadar olan düzeylerin başlıklarını ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir taslak içerecektir.
// Bu taslaktaki bir girişe tıklamak bizi ilgili başlığın konumuna götürecektir.
// Seviyeleri 4'ün üzerinde olan tüm başlıkları anahattan hariç tutmak için "HeadingsOutlineLevels" özelliğini "4" olarak ayarlayın.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Bir anahat girişinin kendisi ile aynı veya daha düşük seviyedeki bir sonraki giriş arasında daha yüksek seviyedeki sonraki girişleri varsa,
// girişin solunda bir ok görünecektir. Bu giriş, bu tür birçok "alt girişin" "sahibidir".
// Belgemizde 5. başlık seviyesindeki taslak girişleri, ikinci 4. seviye taslak girişinin alt girişleridir,
// 4. ve 5. başlık seviyesi girişleri, ikinci 3. seviye girişinin alt girişleridir, vb.
// Ana hatlarıyla, tüm alt girişlerini daraltmak/genişletmek için "sahip" girişinin okuna tıklayabiliriz.
// Tüm başlık düzeyi 2'yi ve alt anahat girişlerini otomatik olarak genişletmek için "ExpandedOutlineLevels" özelliğini "2" olarak ayarlayın
// ve belgeyi açtığımızda tüm seviye ve 3 ve üzeri girişleri daraltıyoruz.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ayrıca bakınız

* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../outlineoptions/)
* toplantı [Aspose.Words](../../../)


