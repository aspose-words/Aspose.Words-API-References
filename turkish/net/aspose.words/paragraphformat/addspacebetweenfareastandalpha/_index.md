---
title: ParagraphFormat.AddSpaceBetweenFarEastAndAlpha
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Geçerli paragrafta Latin metninin Region ve Doğu Asya metninin bölgeleri arasında karakterler arası aralığın otomatik olarak ayarlanıp ayarlanmadığını belirten bir bayrak alır veya ayarlar.
type: docs
weight: 10
url: /tr/net/aspose.words/paragraphformat/addspacebetweenfareastandalpha/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndAlpha property

Geçerli paragrafta, Latin metninin Region ve Doğu Asya metninin bölgeleri arasında karakterler arası aralığın otomatik olarak ayarlanıp ayarlanmadığını belirten bir bayrak alır veya ayarlar.

```csharp
public bool AddSpaceBetweenFarEastAndAlpha { get; set; }
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

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


