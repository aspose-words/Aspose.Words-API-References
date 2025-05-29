---
title: ParagraphFormat.AddSpaceBetweenFarEastAndAlpha
linktitle: AddSpaceBetweenFarEastAndAlpha
articleTitle: AddSpaceBetweenFarEastAndAlpha
second_title: .NET için Aspose.Words
description: ParagraphFormat AddSpaceBetweenFarEastAndAlpha özelliğiyle belgenizin görünümünü en iyi duruma getirin ve Latin ve Doğu Asya metinleri arasındaki boşlukları artırın.
type: docs
weight: 10
url: /tr/net/aspose.words/paragraphformat/addspacebetweenfareastandalpha/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndAlpha property

Latin metin bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakter aralığının otomatik olarak ayarlanıp ayarlanmadığını belirten bir bayrak alır veya ayarlar.

```csharp
public bool AddSpaceBetweenFarEastAndAlpha { get; set; }
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
