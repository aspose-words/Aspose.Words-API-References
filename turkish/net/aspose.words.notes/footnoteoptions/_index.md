---
title: FootnoteOptions Class
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: .NET için Aspose.Words
description: Belgelerinizde ve bölümlerinizde özelleştirilebilir dipnot numaralandırması için Aspose.Words.FootnoteOptions sınıfını keşfedin. Belgenizin netliğini bugün artırın!
type: docs
weight: 4970
url: /tr/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

Bir belge veya bölüm için dipnot numaralandırma seçeneklerini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dipnot ve Sonnot ile Çalışma](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) belgeleme makalesi.

```csharp
public sealed class FootnoteOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | Dipnot alanının biçimlendirileceği sütun sayısını belirtir. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | Otomatik olarak numaralandırılan dipnotlar için sayı biçimini belirtir. |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | Dipnotların konumunu belirtir. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | Otomatik numaralandırmanın ne zaman yeniden başlayacağını belirler. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | İlk otomatik olarak numaralandırılan dipnotlar için başlangıç numarasını veya karakteri belirtir. |

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

// Dipnot, metne bir referans veya yan yorum eklemenin bir yoludur
 // ana gövde metninin akışını engellemeyen.
// Dipnot eklemek, küçük bir üst simge referans sembolü ekler
// Dipnotu eklediğimiz ana metinde.
// Her dipnot ayrıca sayfanın en altında bir giriş oluşturur ve bu giriş bir sembolden oluşur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertFootnote" metoduna geçirdiğimiz referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Belgenin tüm dipnotlarının nereye yerleştirileceğini belirlemek için "Konum" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "FootnotePosition.BottomOfPage" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfanın en altında görünecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "FootnotePosition.BeneathText" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfanın metninin sonunda görünecektir.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Belgenin dipnot/sonnot sayımının başlayacağı sayının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar metne bir referans veya yan yorum eklemenin bir yoludur
 // ana gövde metninin akışını engellemeyen.
// Dipnot/sonnot eklemek küçük bir üst simge referans sembolü ekler
// Dipnot/Sonnotu eklediğimiz ana metin gövdesinde.
// Her dipnot/sonnot ayrıca bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertEndnote" metoduna geçirdiğimiz referans metni.
// Dipnot girişleri, varsayılan olarak, aşağıdaki bilgileri içeren her sayfanın altında gösterilir:
// referans sembolleri ve dipnotlar belgenin sonunda gösterilir.
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

// Varsayılan olarak, her dipnot ve sonnot için referans sembolü onun dizinidir
// belgenin tüm dipnotları/sonnotları arasında. Her belge ayrı sayımları korur
// dipnotlar ve sonnotlar için, her ikisi de 1'den başlar.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Belgeyi almak için "StartNumber" özelliğini kullanabiliriz
// Dipnot veya sonnot sayımını farklı bir numaradan başlat.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Dipnot/sonnot referans işaretlerinin numara stilinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar metne bir referans veya yan yorum eklemenin bir yoludur
 // ana gövde metninin akışını engellemeyen.
// Dipnot/sonnot eklemek küçük bir üst simge referans sembolü ekler
// Dipnot/Sonnotu eklediğimiz ana metin gövdesinde.
// Her dipnot/sonnot ayrıca referansla eşleşen bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki sembol. Belge oluşturucunun "InsertEndnote" metoduna geçirdiğimiz referans metni.
// Dipnot girişleri, varsayılan olarak, aşağıdaki bilgileri içeren her sayfanın altında gösterilir:
// referans sembolleri ve dipnotlar belgenin sonunda gösterilir.
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

// Varsayılan olarak, her dipnot ve sonnot için referans sembolü onun dizinidir
// belgenin tüm dipnotları/sonnotları arasında. Her belge ayrı sayımları korur
// dipnotlar ve son notlar için. Varsayılan olarak, dipnotlar numaralarını Arap rakamları kullanarak görüntüler,
// ve dipnotlarda numaralar küçük harfli Roma rakamlarıyla gösterilir.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Dipnotlara ve son notlara özel numaralandırma stilleri uygulamak için "NumberStyle" özelliğini kullanabiliriz.
// Bu, özel referans işaretlerine sahip dipnotları/sonnotları etkilemeyecektir.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Belgenin belirli yerlerinde dipnot/sonnot numaralandırmasının nasıl yeniden başlatılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnotlar ve son notlar metne bir referans veya yan yorum eklemenin bir yoludur
 // ana gövde metninin akışını engellemeyen.
// Dipnot/sonnot eklemek küçük bir üst simge referans sembolü ekler
// Dipnot/Sonnotu eklediğimiz ana metin gövdesinde.
// Her dipnot/sonnot ayrıca referansla eşleşen bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki sembol. Belge oluşturucunun "InsertEndnote" metoduna geçirdiğimiz referans metni.
// Dipnot girişleri, varsayılan olarak, aşağıdaki bilgileri içeren her sayfanın altında gösterilir:
// referans sembolleri ve dipnotlar belgenin sonunda gösterilir.
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

// Varsayılan olarak, her dipnot ve sonnot için referans sembolü onun dizinidir
// belgenin tüm dipnotları/sonnotları arasında. Her belge ayrı sayımları korur
// dipnotlar ve sonnotlar için geçerlidir ve bu sayımları hiçbir noktada yeniden başlatmaz.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Belgenin yeniden başlatılmasını sağlamak için "RestartRule" özelliğini kullanabiliriz
// Dipnot/Sonnot yeni bir sayfa veya bölümde sayılır.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Ayrıca bakınız

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
