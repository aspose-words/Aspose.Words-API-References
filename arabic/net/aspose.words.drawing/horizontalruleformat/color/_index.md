---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: HorizontalRuleFormat Color ملكية. الحصول على أو تعيين لون الفرشاة الذي يملأ القاعدة الأفقية في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

الحصول على أو تعيين لون الفرشاة الذي يملأ القاعدة الأفقية.

```csharp
public Color Color { get; set; }
```

## ملاحظات

هذا اختصار لل[`Color`](../../fill/color/) ملكية.

القيمة الافتراضية هي Gray.

## أمثلة

يوضح كيفية إدراج شكل قاعدة أفقية، وتخصيص تنسيقه.

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

### أنظر أيضا

* class [HorizontalRuleFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
