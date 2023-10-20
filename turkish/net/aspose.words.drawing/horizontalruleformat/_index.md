---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.HorizontalRuleFormat sınıf. Yatay kural biçimlendirmesini temsil eder C#'da.
type: docs
weight: 1050
url: /tr/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Yatay kural biçimlendirmesini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Şekillerle Çalışmak](https://docs.aspose.com/words/net/working-with-shapes/) dokümantasyon makalesi.

```csharp
public class HorizontalRuleFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Yatay kuralın hizalamasını alır veya ayarlar. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Yatay kuralı dolduran fırça rengini alır veya ayarlar. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Yatay kuralın yüksekliğini alır veya ayarlar. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Yatay cetvel için 3 boyutlu gölgelemenin varlığını belirtir. If`doğru` bu durumda yatay çizgi 3 boyutlu gölgeleme olmadan düz renk kullanılır. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Pencere genişliğinin yüzdesi olarak ifade edilen, belirtilen yatay kuralın uzunluğunu alır veya ayarlar. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
