---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertParagraph yöntem. Belgeye paragraf sonu ekler C#'da.
type: docs
weight: 420
url: /tr/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Belgeye paragraf sonu ekler.

```csharp
public Paragraph InsertParagraph()
```

### Geri dönüş değeri

Az önce eklenen paragraf düğümü. Bu aynı düğüm[`CurrentParagraph`](../currentparagraph/).

## Notlar

Tarafından belirtilen geçerli paragraf biçimlendirmesi[`ParagraphFormat`](../paragraphformat/) mülkiyet kullanılır.

Geçerli paragrafı ikiye böler. Paragrafı ekledikten sonra imleç yeni paragrafın başına yerleştirilir.

Geçerli imleç konumuna paragraf sonu eklemek mümkün değilse bir istisna oluşturulur.

## Örnekler

Belgeye nasıl paragraf ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// "Writeln" yöntemi, metin eklendikten sonra paragrafı sonlandırır
// ve ardından yeni bir paragraf ekleyerek yeni bir satır başlatır.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
