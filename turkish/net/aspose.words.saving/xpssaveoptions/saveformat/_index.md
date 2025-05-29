---
title: XpsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Belgenizin nasıl kaydedileceğini tanımlayan XpsSaveOptions SaveFormat özelliğini keşfedin. Sorunsuz belge işleme için en uygun XPS biçimini sağlayın!
type: docs
weight: 40
url: /tr/net/aspose.words.saving/xpssaveoptions/saveformat/
---
## XpsSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaXps .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Örnekler

Kaydedilmiş bir XPS belgesinin ana hatlarında görünecek başlıkların düzeyinin nasıl sınırlandırılacağını gösterir.

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

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e nasıl dönüştüreceğini değiştirmek için.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Çıktı XPS belgesi, belge gövdesindeki başlıkları listeleyen bir içerik tablosu olan bir ana hat içerecektir.
// Bu taslaktaki bir girdiye tıkladığımızda ilgili başlığın bulunduğu yere gideceğiz.
// Anahattan 2'nin üstündeki tüm başlıkları hariç tutmak için "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayın.
// Yukarıda eklediğimiz son iki başlık görünmeyecektir.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
