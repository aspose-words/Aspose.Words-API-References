---
title: ParagraphFormat.IsHeading
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Paragraf stili yerleşik Başlık stillerinden biri olduğunda doğrudur.
type: docs
weight: 130
url: /tr/net/aspose.words/paragraphformat/isheading/
---
## ParagraphFormat.IsHeading property

Paragraf stili yerleşik Başlık stillerinden biri olduğunda doğrudur.

```csharp
public bool IsHeading { get; }
```

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

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


