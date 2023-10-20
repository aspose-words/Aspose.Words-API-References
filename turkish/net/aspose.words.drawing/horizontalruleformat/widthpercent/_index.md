---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: Aspose.Words for .NET
description: HorizontalRuleFormat WidthPercent mülk. Pencere genişliğinin yüzdesi olarak ifade edilen belirtilen yatay kuralın uzunluğunu alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Pencere genişliğinin yüzdesi olarak ifade edilen, belirtilen yatay kuralın uzunluğunu alır veya ayarlar.

```csharp
public double WidthPercent { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Bağımsız değişken geçerli değerler aralığının dışında olduğunda atar. |

## Notlar

Geçerli değerler 1'den 100'e kadar değişir.

Varsayılan değer 100'dür.

## Örnekler

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
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
