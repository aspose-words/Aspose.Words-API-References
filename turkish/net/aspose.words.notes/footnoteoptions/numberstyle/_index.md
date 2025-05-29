---
title: FootnoteOptions.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: .NET için Aspose.Words
description: Gelişmiş belge netliği ve profesyonelliği için dipnot numaralandırma biçimlerini kolayca özelleştirmek üzere FootnoteOptions NumberStyle özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.notes/footnoteoptions/numberstyle/
---
## FootnoteOptions.NumberStyle property

Otomatik olarak numaralandırılan dipnotlar için sayı biçimini belirtir.

```csharp
public NumberStyle NumberStyle { get; set; }
```

## Notlar

Tüm sayı stilleri bu özellik için geçerli değildir. Uygulanabilir sayı stilleri listesi için Microsoft Word'deki Dipnot veya Sonnot Ekle iletişim kutusuna bakın. Uygulanabilir olmayan bir sayı stili seçerseniz, Microsoft Word varsayılan bir değere geri döner.

## Örnekler

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

### Ayrıca bakınız

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [FootnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
