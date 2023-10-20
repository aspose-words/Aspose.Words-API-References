---
title: FootnoteNumberingRule Enum
linktitle: FootnoteNumberingRule
articleTitle: FootnoteNumberingRule
second_title: Aspose.Words for .NET
description: Aspose.Words.Notes.FootnoteNumberingRule Sıralama. Otomatik dipnot veya sonnot numaralandırmanın ne zaman yeniden başlayacağını belirler C#'da.
type: docs
weight: 4270
url: /tr/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

Otomatik dipnot veya sonnot numaralandırmanın ne zaman yeniden başlayacağını belirler.

```csharp
public enum FootnoteNumberingRule
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Continuous | `0` | Belge boyunca sürekli numaralandırma. |
| RestartSection | `1` | Numaralandırma her bölümde yeniden başlar. |
| RestartPage | `2` | Numaralandırma her sayfada yeniden başlar. Yalnızca dipnotlar için geçerlidir. |
| Default | `0` | EşittirContinuous . |

## Örnekler

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

* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
