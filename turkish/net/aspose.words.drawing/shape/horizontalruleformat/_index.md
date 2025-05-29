---
title: Shape.HorizontalRuleFormat
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım esnekliği için YatayRuleFormat özelliklerine erişin ve özelleştirin. Benzersiz sonuçlar için şekillerinizi özelleştirilmiş ayarlarla optimize edin.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Yatay kural şeklinin özelliklerine erişim sağlar. Yatay kural olmayan bir şekil için, şunu döndürür:`hükümsüz` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
