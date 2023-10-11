---
title: Shape.HorizontalRuleFormat
second_title: Aspose.Words for .NET API Referansı
description: Shape mülk. Yatay kural şeklinin özelliklerine erişim sağlar. Yatay kural olmayan bir şekil için şunu döndürürhükümsüz .
type: docs
weight: 100
url: /tr/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Yatay kural şeklinin özelliklerine erişim sağlar. Yatay kural olmayan bir şekil için şunu döndürür:`hükümsüz` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../shape/)
* toplantı [Aspose.Words](../../../)


