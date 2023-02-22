---
title: EndnoteOptions.StartNumber
second_title: Aspose.Words for .NET API Referansı
description: EndnoteOptions mülk. İlk otomatik olarak numaralandırılmış son notlar için başlangıç numarasını veya karakterini belirtir.
type: docs
weight: 40
url: /tr/net/aspose.words.notes/endnoteoptions/startnumber/
---
## EndnoteOptions.StartNumber property

İlk otomatik olarak numaralandırılmış son notlar için başlangıç numarasını veya karakterini belirtir.

```csharp
public int StartNumber { get; set; }
```

### Notlar

Bu özellik yalnızca şu durumlarda etkilidir:[`RestartRule`](../restartrule/) olarak ayarlandıContinuous.

### Örnekler

Belgenin dipnot/son not sayımına başladığı bir sayının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar, metne referans veya yan yorum eklemenin bir yoludur
// ana gövde metninin akışını engellemez. 
// Bir dipnot/sonnot eklemek, küçük bir üst simge referans sembolü ekler
// dipnotu/son notu eklediğimiz ana gövde metninde.
// Her dipnot/sonnot ayrıca bir sembolden oluşan bir giriş oluşturur.
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertEndnote" yöntemine aktardığımız referans metni.
// Dipnot girişleri, varsayılan olarak, aşağıdakileri içeren her sayfanın altında görünür:
// referans sembolleri ve son notları belgenin sonunda görünür.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// Varsayılan olarak, her dipnot ve son not için referans sembolü, onun indeksidir.
// tüm belgenin dipnotları/son notları arasında. Her belge ayrı sayıları tutar
// her ikisi de 1'den başlayan dipnotlar ve son notlar için.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Belgeyi almak için "StartNumber" özelliğini kullanabiliriz.
// bir dipnota veya son not sayımına farklı bir sayı ile başlayın.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### Ayrıca bakınız

* class [EndnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../endnoteoptions/)
* toplantı [Aspose.Words](../../../)


