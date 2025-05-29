---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: .NET için Aspose.Words
description: Daha iyi tasarım kontrolü için yatay kuralınızın uzunluğunu pencere genişliğinin yüzdesi olarak kolayca özelleştirmek üzere YatayRuleFormat WidthPercent özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Belirtilen yatay kuralın uzunluğunu pencere genişliğinin yüzdesi olarak ifade eder veya ayarlar.

```csharp
public double WidthPercent { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Argüman geçerli değerler aralığının dışında olduğunda fırlatılır. |

## Notlar

Geçerli değerler 1 ile 100 (dahil) arasındadır.

Varsayılan değer 100'dür.

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
