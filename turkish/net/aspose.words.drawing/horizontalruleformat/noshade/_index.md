---
title: HorizontalRuleFormat.NoShade
linktitle: NoShade
articleTitle: NoShade
second_title: .NET için Aspose.Words
description: YatayRuleFormat NoShade özelliğini keşfedin, yatay çizgiler için 3B gölgelendirmeyi kontrol edin. Zahmetsizce şık, düz renkli bir tasarıma ulaşın!
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Yatay kural için 3B gölgelendirmenin varlığını gösterir. Eğer`doğru` , o zaman yatay kural 3D gölgelendirme olmadan ve düz renk kullanılarak yapılır.

```csharp
public bool NoShade { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ`.

## Örnekler

Yatay çizgi şeklinin nasıl ekleneceğini ve biçimlendirmesinin nasıl özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertHorizontalRule();

HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
horizontalRuleFormat.WidthPercent = 70;
horizontalRuleFormat.Height = 3;
horizontalRuleFormat.Color = Color.Blue;
horizontalRuleFormat.NoShade = true;

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### Ayrıca bakınız

* class [HorizontalRuleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
