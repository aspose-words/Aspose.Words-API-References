---
title: EndnoteOptions Class
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: .NET için Aspose.Words
description: Belgelerinizde ve bölümlerinizde özelleştirilebilir son not numaralandırması için Aspose.Words EndnoteOptions sınıfını keşfedin. Belge biçimlendirmenizi bugün geliştirin!
type: docs
weight: 4930
url: /tr/net/aspose.words.notes/endnoteoptions/
---
## EndnoteOptions class

Bir belge veya bölüm için dipnot numaralandırma seçeneklerini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dipnot ve Sonnot ile Çalışma](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) belgeleme makalesi.

```csharp
public sealed class EndnoteOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [NumberStyle](../../aspose.words.notes/endnoteoptions/numberstyle/) { get; set; } | Otomatik olarak numaralandırılan dipnotlar için sayı biçimini belirtir. |
| [Position](../../aspose.words.notes/endnoteoptions/position/) { get; set; } | Dipnotların konumunu belirtir. |
| [RestartRule](../../aspose.words.notes/endnoteoptions/restartrule/) { get; set; } | Otomatik numaralandırmanın ne zaman yeniden başlayacağını belirler. |
| [StartNumber](../../aspose.words.notes/endnoteoptions/startnumber/) { get; set; } | İlk otomatik olarak numaralandırılan dipnotlar için başlangıç numarasını veya karakteri belirtir. |

## Örnekler

Belgenin dipnotlarını toplayıp görüntüleyeceği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Son not, metne bir referans veya yan yorum eklemenin bir yoludur
 // ana gövde metninin akışını engellemeyen.
// Bir dipnot eklemek, küçük bir üst simge referans sembolü ekler
// dipnotu eklediğimiz ana metinde.
// Her dipnot ayrıca belgenin sonunda bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertEndnote" metoduna geçirdiğimiz referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Belgenin tüm dipnotlarının nereye yerleştirileceğini belirlemek için "Konum" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "EndnotePosition.EndOfDocument" olarak ayarlarsak,
// her dipnot belgenin sonunda bir koleksiyonda gösterilecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "EndnotePosition.EndOfSection" olarak ayarlarsak,
// her dipnot, dipnotun referans işaretini içeren bölümün sonundaki bir koleksiyonda görünecektir.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
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

* property [EndnoteOptions](../../aspose.words/document/endnoteoptions/)
* property [EndnoteOptions](../../aspose.words/pagesetup/endnoteoptions/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
