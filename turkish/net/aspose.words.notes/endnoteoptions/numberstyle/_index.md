---
title: EndnoteOptions.NumberStyle
second_title: Aspose.Words for .NET API Referansı
description: EndnoteOptions mülk. Otomatik olarak numaralandırılan son notlar için sayı biçimini belirtir.
type: docs
weight: 10
url: /tr/net/aspose.words.notes/endnoteoptions/numberstyle/
---
## EndnoteOptions.NumberStyle property

Otomatik olarak numaralandırılan son notlar için sayı biçimini belirtir.

```csharp
public NumberStyle NumberStyle { get; set; }
```

### Notlar

Bu özellik için tüm sayı stilleri geçerli değildir. Uygulanabilir sayı stillerinin listesi için Microsoft Word'deki Dipnot veya Sonnot Ekle iletişim kutusuna bakın. Uygun olmayan bir sayı stilini seçerseniz, Microsoft Word varsayılan değere geri döner.

### Örnekler

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

### Ayrıca bakınız

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [EndnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../endnoteoptions/)
* toplantı [Aspose.Words](../../../)


