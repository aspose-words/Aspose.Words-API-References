---
title: FootnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: .NET için Aspose.Words
description: Dipnot numaralandırmanızı özelleştirmek, belge netliğini ve organizasyonunu zahmetsizce artırmak için FootnoteOptions StartNumber özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.notes/footnoteoptions/startnumber/
---
## FootnoteOptions.StartNumber property

İlk otomatik olarak numaralandırılan dipnotlar için başlangıç numarasını veya karakteri belirtir.

```csharp
public int StartNumber { get; set; }
```

## Notlar

Bu özellik yalnızca şu durumlarda etkilidir:[`RestartRule`](../restartrule/)x000d_ olarak ayarlandıContinuous.

## Örnekler

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

### Ayrıca bakınız

* class [FootnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
