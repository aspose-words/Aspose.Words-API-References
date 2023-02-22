---
title: HorizontalRuleFormat.Alignment
second_title: Aspose.Words for .NET API Referansı
description: HorizontalRuleFormat mülk. Yatay kuralın hizalamasını alır veya ayarlar.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Yatay kuralın hizalamasını alır veya ayarlar.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

### Notlar

Varsayılan değerLeft.

### Örnekler

Yatay bir kural şeklinin nasıl ekleneceğini ve biçimlendirmesinin nasıl özelleştirileceğini gösterir.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../horizontalruleformat/)
* toplantı [Aspose.Words](../../../)


