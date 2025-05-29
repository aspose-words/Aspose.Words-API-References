---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: .NET için Aspose.Words
description: Belgelerinizi DocumentBuilder InsertParagraph yöntemiyle zahmetsizce geliştirin; okunabilirliği artırmak için kusursuz paragraf sonları oluşturun.
type: docs
weight: 450
url: /tr/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Belgeye bir paragraf sonu ekler.

```csharp
public Paragraph InsertParagraph()
```

### Geri dönüş değeri

Az önce eklenen paragraf düğümü. Aynı düğümdür[`CurrentParagraph`](../currentparagraph/).

## Notlar

Mevcut paragraf biçimlendirmesi, tarafından belirtilmiştir[`ParagraphFormat`](../paragraphformat/) mülk kullanılır.

Mevcut paragrafı ikiye böler. Paragraf eklendikten sonra imleç yeni paragrafın başına yerleştirilir.

Mevcut imleç konumuna paragraf sonu eklemek mümkün değilse bir istisna atılır.

## Örnekler

Belgeye bir paragrafın nasıl ekleneceğini gösterir.

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

// "Writeln" yöntemi, metni ekledikten sonra paragrafı sonlandırır
// ve ardından yeni bir satır başlatır ve yeni bir paragraf ekler.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
