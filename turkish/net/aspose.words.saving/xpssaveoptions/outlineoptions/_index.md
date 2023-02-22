---
title: XpsSaveOptions.OutlineOptions
second_title: Aspose.Words for .NET API Referansı
description: XpsSaveOptions mülk. Anahat seçeneklerini belirlemeye izin verir.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Anahat seçeneklerini belirlemeye izin verir.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Notlar

XPS'e kaydederken ExpandedOutlineLevels seçeneğinin çalışmayacağını unutmayın.

### Örnekler

Kaydedilmiş bir XPS belgesinin ana hatlarında görünecek başlıkların düzeyinin nasıl sınırlandırılacağını gösterir.

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

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'ye dönüştürme şeklini değiştirmek için.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Çıktı XPS belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir anahat içerecektir.
// Bu taslakta bir girdiye tıklamak bizi ilgili başlığın konumuna götürecektir.
// Seviyeleri 2'nin üzerinde olan tüm başlıkları anahattan çıkarmak için "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayın.
// Yukarıda eklediğimiz son iki başlık görünmeyecektir.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ayrıca bakınız

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../xpssaveoptions/)
* toplantı [Aspose.Words](../../../)


