---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: .NET için Aspose.Words
description: Gelişmiş yatay kural biçimlendirmesi için Aspose.Words.Drawing.HorizontalRuleFormat sınıfını keşfedin. Belge tasarımınızı zahmetsizce geliştirin!
type: docs
weight: 1380
url: /tr/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Yatay kural biçimlendirmesini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Şekillerle Çalışma](https://docs.aspose.com/words/net/working-with-shapes/) belgeleme makalesi.

```csharp
public class HorizontalRuleFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Yatay kuralın hizalamasını alır veya ayarlar. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Yatay kuralı dolduran fırça rengini alır veya ayarlar. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Yatay kuralın yüksekliğini alır veya ayarlar. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Yatay kural için 3B gölgelendirmenin varlığını gösterir. Eğer`doğru` , o zaman yatay kural 3D gölgelendirme olmadan ve düz renk kullanılarak yapılır. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Belirtilen yatay kuralın uzunluğunu pencere genişliğinin yüzdesi olarak ifade eder veya ayarlar. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
