---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: .NET için Aspose.Words
description: Yatay kural hizalaması üzerinde hassas kontrol sağlamak, belge biçimlendirmenizi ve tasarımınızı geliştirmek için Aspose.Words.HorizontalRuleAlignment numaralandırmasını keşfedin.
type: docs
weight: 1370
url: /tr/net/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enumeration

Belirtilen yatay kural için hizalamayı temsil eder.

```csharp
public enum HorizontalRuleAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Left | `0` | Sola hizalanmış. |
| Center | `1` | Merkeze hizalanmış. |
| Right | `2` | Sağa hizalanmış. |

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
