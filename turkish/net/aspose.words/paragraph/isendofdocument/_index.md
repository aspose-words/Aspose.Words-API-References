---
title: Paragraph.IsEndOfDocument
second_title: Aspose.Words for .NET API Referansı
description: Paragraph mülk. Bu paragraf belgenin son bölümündeki son paragrafsa doğrudur.
type: docs
weight: 60
url: /tr/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Bu paragraf belgenin son bölümündeki son paragrafsa doğrudur.

```csharp
public bool IsEndOfDocument { get; }
```

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

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)


