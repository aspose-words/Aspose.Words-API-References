---
title: FootnoteOptions.RestartRule
linktitle: RestartRule
articleTitle: RestartRule
second_title: .NET için Aspose.Words
description: Otomatik numaralandırma sıfırlamalarını kontrol etmek, belge organizasyonunu ve netliğini artırmak için FootnoteOptions RestartRule özelliğini keşfedin. İş akışınızı bugün optimize edin!
type: docs
weight: 40
url: /tr/net/aspose.words.notes/footnoteoptions/restartrule/
---
## FootnoteOptions.RestartRule property

Otomatik numaralandırmanın ne zaman yeniden başlayacağını belirler.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

## Örnekler

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

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [FootnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
