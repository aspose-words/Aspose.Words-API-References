---
title: ShapeBase.IsHorizontalRule
linktitle: IsHorizontalRule
articleTitle: IsHorizontalRule
second_title: .NET için Aspose.Words
description: ShapeBase IsHorizontalRule özelliğini keşfedin, tasarımlarınızda yatay çizgileri kolayca tanımlayarak düzen ve stil verimliliğini artırın.
type: docs
weight: 290
url: /tr/net/aspose.words.drawing/shapebase/ishorizontalrule/
---
## ShapeBase.IsHorizontalRule property

Geri Döndürür`doğru` eğer bu şekil yatay bir cetvel ise.

```csharp
public bool IsHorizontalRule { get; }
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

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
