---
title: DocumentBuilder.InsertHorizontalRule
linktitle: InsertHorizontalRule
articleTitle: InsertHorizontalRule
second_title: .NET için Aspose.Words
description: Belgelerinizi DocumentBuilder InsertHorizontalRule yöntemiyle geliştirin, daha iyi bir organizasyon ve görsel çekicilik için şık yatay çizgiler ekleyin.
type: docs
weight: 370
url: /tr/net/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder.InsertHorizontalRule method

Belgeye yatay bir kural şekli ekler.

```csharp
public Shape InsertHorizontalRule()
```

### Geri dönüş değeri

Yatay cetvel olan şekil.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
