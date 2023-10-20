---
title: FootnoteOptions Class
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Notes.FootnoteOptions sınıf. Bir belge veya bölüme ilişkin dipnot numaralandırma seçeneklerini temsil eder C#'da.
type: docs
weight: 4280
url: /tr/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

Bir belge veya bölüme ilişkin dipnot numaralandırma seçeneklerini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Dipnot ve Sonnot ile Çalışmak](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) dokümantasyon makalesi.

```csharp
public sealed class FootnoteOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | Dipnot alanının formatlanacağı sütun sayısını belirtir. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | Otomatik olarak numaralandırılan dipnotların sayı biçimini belirtir. |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | Dipnotların konumunu belirtir. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | Otomatik numaralandırmanın ne zaman yeniden başlayacağını belirler. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | Otomatik olarak numaralandırılan ilk dipnotların başlangıç numarasını veya karakterini belirtir. |

## Örnekler

Dipnot bölümünün belirli sayıda sütuna nasıl bölüneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

Belgenin dipnotlarını toplayıp görüntüleyeceği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnot, metne referans veya yan yorum eklemenin bir yoludur
 // bu, ana gövde metninin akışına müdahale etmez.
// Dipnot eklemek küçük bir üst simge referans sembolü ekler
// ana gövde metninde dipnotu eklediğimiz yere.
// Her dipnot ayrıca sayfanın altında bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertFootnote" yöntemine ilettiğimiz referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Belgenin tüm dipnotlarını nereye yerleştireceğini belirlemek için "Konum" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "FootnotePosition.BottomOfPage" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfanın altında görünecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "FootnotePosition.BeneathText" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfa metninin sonunda görünecektir.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
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

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
