---
title: OutlineOptions.HeadingsOutlineLevels
linktitle: HeadingsOutlineLevels
articleTitle: HeadingsOutlineLevels
second_title: .NET için Aspose.Words
description: OutlineOptions'da HeadingsOutlineLevels özelliğini keşfedin. Yapılandırılmış belgeler için başlık düzeylerini kontrol edin ve gezinmeyi kolaylıkla geliştirin.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

belge taslağına kaç düzeyde başlık (Başlık stilleri ile biçimlendirilmiş paragraflar) ekleneceğini belirtir.

```csharp
public int HeadingsOutlineLevels { get; set; }
```

## Notlar

Anahatta hiç başlık yoksa 0 belirtin; anahatta tek düzey başlık varsa 1 belirtin, vb.

Varsayılan 0'dır. Geçerli aralık 0 ila 9'dur.

## Örnekler

Belgenin tamamının üç düzeyde PDF'ye nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 1'den 5'e kadar olan seviyelerin başlıklarını ekleyin.
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

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içerik tablosu olan bir ana hat içerecektir.
// Bu taslaktaki bir girdiye tıkladığımızda ilgili başlığın bulunduğu yere gideceğiz.
// Anahattan 4'ün üstündeki tüm başlıkları hariç tutmak için "HeadingsOutlineLevels" özelliğini "4" olarak ayarlayın.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Bir ana hat girişinin kendisi ile aynı veya daha düşük seviyedeki bir sonraki giriş arasında daha yüksek seviyede müteakip girişler varsa,
// girişin solunda bir ok belirecektir. Bu giriş, bu tür birkaç "alt girişin" "sahibi"dir.
// Belgemizde, 5. başlık seviyesindeki ana hat girişleri, ikinci 4. seviye ana hat girişinin alt girişleridir.
// 4. ve 5. başlık seviyesi girişleri, 2. 3. seviye girişin alt girişleridir, vb.
// Anahatta, "sahip" girişinin okuna tıklayarak tüm alt girişlerini daraltabilir/genişletebiliriz.
// Tüm başlık düzeyi 2 ve alt anahat girişlerini otomatik olarak genişletmek için "ExpandedOutlineLevels" özelliğini "2" olarak ayarlayın
// ve belgeyi açtığımızda tüm seviye ve 3 ve üzeri girdileri daraltırız.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ayrıca bakınız

* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
