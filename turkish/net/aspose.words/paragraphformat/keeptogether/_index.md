---
title: ParagraphFormat.KeepTogether
linktitle: KeepTogether
articleTitle: KeepTogether
second_title: .NET için Aspose.Words
description: ParagraphFormat KeepTogether özelliğini keşfedin, belge okunabilirliğini artırmak ve profesyonel sunum için tüm satırların tek bir sayfada bir arada kalmasını sağlayın.
type: docs
weight: 160
url: /tr/net/aspose.words/paragraphformat/keeptogether/
---
## ParagraphFormat.KeepTogether property

Paragraftaki tüm satırların aynı sayfada kalması gerekiyorsa doğrudur.

```csharp
public bool KeepTogether { get; set; }
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

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
