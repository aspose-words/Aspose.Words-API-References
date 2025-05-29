---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: .NET için Aspose.Words
description: Yatay Kuralınızın yüksekliğini kolayca ayarlayın. Web projelerinizde özelleştirilebilir tasarım için Yükseklik özelliğini keşfedin. Düzeninizi bugün geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

Yatay kuralın yüksekliğini alır veya ayarlar.

```csharp
public double Height { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Argüman geçerli değerler aralığının dışında olduğunda fırlatılır. |

## Notlar

Bu, şuna giden bir kısayoldur:[`Height`](../../shapebase/height/) mülk.

Geçerli değerler 0 ile 1584 (dahil) arasındadır.

Varsayılan değer 1,5'tir.

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
