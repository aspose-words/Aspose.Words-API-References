---
title: HorizontalRuleFormat.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım esnekliği için yatay kuralların hizalamasını kolayca özelleştirmek amacıyla YatayKuralBiçim Hizalama özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Yatay kuralın hizalamasını alır veya ayarlar.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

## Notlar

Varsayılan değer:Left.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
