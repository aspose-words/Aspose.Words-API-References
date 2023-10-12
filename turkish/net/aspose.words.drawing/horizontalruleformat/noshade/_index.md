---
title: HorizontalRuleFormat.NoShade
second_title: Aspose.Words for .NET API Referansı
description: HorizontalRuleFormat mülk. Yatay cetvel için 3 boyutlu gölgelemenin varlığını belirtir. Ifdoğru bu durumda yatay çizgi 3 boyutlu gölgeleme olmadan düz renk kullanılır.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Yatay cetvel için 3 boyutlu gölgelemenin varlığını belirtir. If`doğru` bu durumda yatay çizgi 3 boyutlu gölgeleme olmadan düz renk kullanılır.

```csharp
public bool NoShade { get; set; }
```

### Notlar

Varsayılan değer:`YANLIŞ`.

### Örnekler

Yatay kural şeklinin nasıl ekleneceğini ve biçimlendirmesinin nasıl özelleştirileceğini gösterir.

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
* ad alanı [Aspose.Words.Drawing](../../horizontalruleformat/)
* toplantı [Aspose.Words](../../../)


