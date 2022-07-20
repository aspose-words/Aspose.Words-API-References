---
title: InsertParagraph
second_title: Aspose.Words for .NET API Referansı
description: Belgeye bir paragraf sonu ekler.
type: docs
weight: 400
url: /tr/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Belgeye bir paragraf sonu ekler.

```csharp
public Paragraph InsertParagraph()
```

### Geri dönüş değeri

Yeni eklenen paragraf düğümü. Aynı düğümdür[`CurrentParagraph`](../currentparagraph).

### Notlar

tarafından belirtilen geçerli paragraf biçimlendirmesi[`ParagraphFormat`](../paragraphformat) mülk kullanılır.

Geçerli paragrafı ikiye böler. Paragrafı yerleştirdikten sonra, imleç yeni paragrafın başına gelir.

### Örnekler

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

// "Writeln" yöntemi, metni ekledikten sonra paragrafı sonlandırır
// ve ardından yeni bir paragraf ekleyerek yeni bir satır başlatır.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph)
* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->