---
title: EndnoteOptions
second_title: Aspose.Words for .NET API Referansı
description: Bu belgedeki son notların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar.
type: docs
weight: 110
url: /tr/net/aspose.words/document/endnoteoptions/
---
## Document.EndnoteOptions property

Bu belgedeki son notların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

### Örnekler

Belgenin son notlarını topladığı ve görüntülediği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Son not, metne referans veya yan yorum eklemenin bir yoludur
// ana gövde metninin akışını engellemez. 
// Bir son not eklemek, küçük bir üst simge referans sembolü ekler
// son notu eklediğimiz ana gövde metninde.
// Her son not ayrıca belgenin sonunda bir sembolden oluşan bir giriş oluşturur.
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertEndnote" yöntemine aktardığımız referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Belgenin tüm son notlarını nereye yerleştireceğini belirlemek için "Position" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "EndnotePosition.EndOfDocument" olarak ayarlarsak,
// her dipnot belgenin sonunda bir koleksiyonda görünecek. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "EndnotePosition.EndOfSection" olarak ayarlarsak,
// her dipnot, metni son notun referans işaretini içeren bölümün sonunda bir koleksiyonda görünecektir.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

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

Dipnot/sonnot referans işaretlerinin sayı stilinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar, metne referans veya yan yorum eklemenin bir yoludur
// ana gövde metninin akışını engellemez. 
// Bir dipnot/sonnot eklemek, küçük bir üst simge referans sembolü ekler
// dipnotu/son notu eklediğimiz ana gövde metninde.
// Her dipnot/sonnot aynı zamanda referansla eşleşen bir sembolden oluşan bir giriş oluşturur.
// ana gövde metninde sembol. Belge oluşturucunun "InsertEndnote" yöntemine ilettiğimiz referans metni.
// Dipnot girişleri, varsayılan olarak, aşağıdakileri içeren her sayfanın altında görünür:
// referans sembolleri ve son notları belgenin sonunda görünür.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// Varsayılan olarak, her dipnot ve son not için referans sembolü, onun indeksidir.
// tüm belgenin dipnotları/son notları arasında. Her belge ayrı sayıları tutar
// dipnotlar ve son notlar için. Varsayılan olarak, dipnotlar numaralarını Arap rakamları kullanarak gösterir,
// ve son notlar numaralarını küçük Romen rakamlarıyla görüntüler.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Dipnotlara ve son notlara özel numaralandırma stilleri uygulamak için "NumberStyle" özelliğini kullanabiliriz.
// Bu, özel referans işaretli dipnotları/son notları etkilemez.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Belgedeki belirli yerlerde dipnot/sonnot numaralandırmanın nasıl yeniden başlatılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar, metne referans veya yan yorum eklemenin bir yoludur
// ana gövde metninin akışını engellemez. 
// Bir dipnot/sonnot eklemek, küçük bir üst simge referans sembolü ekler
// dipnotu/son notu eklediğimiz ana gövde metninde.
// Her dipnot/sonnot aynı zamanda referansla eşleşen bir sembolden oluşan bir giriş oluşturur.
// ana gövde metninde sembol. Belge oluşturucunun "InsertEndnote" yöntemine ilettiğimiz referans metni.
// Dipnot girişleri, varsayılan olarak, aşağıdakileri içeren her sayfanın altında görünür:
// referans sembolleri ve son notları belgenin sonunda görünür.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// Varsayılan olarak, her dipnot ve son not için referans sembolü, onun indeksidir.
// tüm belgenin dipnotları/son notları arasında. Her belge ayrı sayıları tutar
// dipnotlar ve son notlar için ve bu sayıları hiçbir noktada yeniden başlatmaz.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Belgeyi yeniden başlatmak için "RestartRule" özelliğini kullanabiliriz
// dipnot/sonnot yeni bir sayfada veya bölümde sayılır.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Ayrıca bakınız

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
