---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: .NET için Aspose.Words
description: Tasarımınızı özelleştirmek için YatayRuleFormat Renk özelliğini keşfedin. Çarpıcı bir yatay kural efekti için fırça rengini kolayca ayarlayın veya alın!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Yatay kuralı dolduran fırça rengini alır veya ayarlar.

```csharp
public Color Color { get; set; }
```

## Notlar

Bu, şuna giden bir kısayoldur:[`Color`](../../fill/color/) mülk.

Varsayılan değer Gray .

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
