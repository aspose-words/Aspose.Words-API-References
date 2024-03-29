---
title: ParagraphFormat.AddSpaceBetweenFarEastAndDigit
linktitle: AddSpaceBetweenFarEastAndDigit
articleTitle: AddSpaceBetweenFarEastAndDigit
second_title: Aspose.Words for .NET
description: ParagraphFormat AddSpaceBetweenFarEastAndDigit mülk. Geçerli paragraftaki Doğu Asya metninin bölgeleri ve bölgeleri arasında karakterlerarası aralığın otomatik olarak ayarlanıp ayarlanmadığını belirten bir bayrak alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/paragraphformat/addspacebetweenfareastanddigit/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndDigit property

Geçerli paragraftaki Doğu Asya metninin bölgeleri ve bölgeleri arasında karakterlerarası aralığın otomatik olarak ayarlanıp ayarlanmadığını belirten bir bayrak alır veya ayarlar.

```csharp
public bool AddSpaceBetweenFarEastAndDigit { get; set; }
```

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

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
