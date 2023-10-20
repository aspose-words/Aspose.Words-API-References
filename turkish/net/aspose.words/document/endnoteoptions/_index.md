---
title: Document.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words for .NET
description: Document EndnoteOptions mülk. Bu belgedeki son notların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words/document/endnoteoptions/
---
## Document.EndnoteOptions property

Bu belgedeki son notların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Örnekler

Belgenin son notlarını toplayıp görüntüleyeceği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Son not, metne bir referans veya yan yorum eklemenin bir yoludur
 // bu, ana gövde metninin akışına müdahale etmez.
// Son notun eklenmesi küçük bir üst simge referans sembolü ekler
// ana gövde metninde son notu eklediğimiz yer.
// Her son not ayrıca belgenin sonunda bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertEndnote" yöntemine ilettiğimiz referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Belgenin tüm son notlarını nereye yerleştireceğini belirlemek için "Konum" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "EndnotePosition.EndOfDocument" olarak ayarlarsak,
// her dipnot belgenin sonunda bir koleksiyonda görünecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "EndnotePosition.EndOfSection" olarak ayarlarsak,
// her dipnot, metni sonnotun referans işaretini içeren bölümün sonunda bir koleksiyonda görünecektir.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

Belgenin dipnot/sonnot sayımına başlayacağı sayının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar metne referans veya yan yorum eklemenin bir yoludur
 // bu, ana gövde metninin akışına müdahale etmez.
// Dipnot/sonnot eklemek küçük bir üst simge referans sembolü ekler
// dipnot/son notu eklediğimiz ana gövde metninde.
// Her dipnot/sonnot ayrıca bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertEndnote" yöntemine ilettiğimiz referans metni.
// Dipnot girişleri varsayılan olarak aşağıdakileri içeren her sayfanın altında görünür:
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

// Varsayılan olarak her dipnot ve son notun referans sembolü onun indeksidir
// belgenin tüm dipnotları/son notları arasında. Her belge ayrı sayımları tutar
// her ikisi de 1'den başlayan dipnotlar ve sonnotlar için.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Belgeyi almak için "BaşlangıçNumber" özelliğini kullanabiliriz
// dipnot veya sonnot sayımına farklı bir numaradan başlayın.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Dipnot/sonnot referans işaretlerinin sayı stilinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar metne referans veya yan yorum eklemenin bir yoludur
 // bu, ana gövde metninin akışına müdahale etmez.
// Dipnot/sonnot eklemek küçük bir üst simge referans sembolü ekler
// dipnot/son notu eklediğimiz ana gövde metninde.
// Her dipnot/sonnot ayrıca referansla eşleşen bir sembolden oluşan bir giriş oluşturur.
// ana gövde metnindeki sembol. Belge oluşturucunun "InsertEndnote" yöntemine ilettiğimiz referans metni.
// Dipnot girişleri varsayılan olarak aşağıdakileri içeren her sayfanın altında görünür:
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

// Varsayılan olarak her dipnot ve son notun referans sembolü onun indeksidir
// belgenin tüm dipnotları/son notları arasında. Her belge ayrı sayımları tutar
// dipnotlar ve sonnotlar için. Dipnotlar varsayılan olarak Arap rakamları kullanılarak numaralarını görüntüler.
// ve son notlar sayılarını küçük Romen rakamlarıyla görüntüler.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Dipnotlara ve sonnotlara özel numaralandırma stilleri uygulamak için "NumberStyle" özelliğini kullanabiliriz.
// Bu, özel referans işaretlerine sahip dipnotları/son notları etkilemeyecektir.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Belgenin belirli yerlerinde dipnot/sonnot numaralandırmasının nasıl yeniden başlatılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar metne referans veya yan yorum eklemenin bir yoludur
 // bu, ana gövde metninin akışına müdahale etmez.
// Dipnot/sonnot eklemek küçük bir üst simge referans sembolü ekler
// dipnot/son notu eklediğimiz ana gövde metninde.
// Her dipnot/sonnot ayrıca referansla eşleşen bir sembolden oluşan bir giriş oluşturur.
// ana gövde metnindeki sembol. Belge oluşturucunun "InsertEndnote" yöntemine ilettiğimiz referans metni.
// Dipnot girişleri varsayılan olarak aşağıdakileri içeren her sayfanın altında görünür:
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

// Varsayılan olarak her dipnot ve son notun referans sembolü onun indeksidir
// belgenin tüm dipnotları/son notları arasında. Her belge ayrı sayımları tutar
// dipnotlar ve sonnotlar için ve bu sayımları herhangi bir noktada yeniden başlatmaz.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Belgenin yeniden başlatılmasını sağlamak için "RestartRule" özelliğini kullanabiliriz
// dipnot/sonnot yeni bir sayfa veya bölümde sayılır.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Ayrıca bakınız

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
