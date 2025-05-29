---
title: Paragraph.IsEndOfDocument
linktitle: IsEndOfDocument
articleTitle: IsEndOfDocument
second_title: .NET için Aspose.Words
description: Paragraflar için IsEndOfDocument özelliğini keşfedin. Etkili biçimlendirme için belgenizin son bölümündeki son paragrafı nasıl tanımlayacağınızı öğrenin.
type: docs
weight: 60
url: /tr/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Bu paragraf belgenin son bölümündeki son paragraf ise doğrudur.

```csharp
public bool IsEndOfDocument { get; }
```

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

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
