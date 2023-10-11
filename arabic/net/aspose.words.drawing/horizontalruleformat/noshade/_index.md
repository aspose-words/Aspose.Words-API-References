---
title: HorizontalRuleFormat.NoShade
second_title: Aspose.Words لمراجع .NET API
description: HorizontalRuleFormat ملكية. يشير إلى وجود تظليل ثلاثي الأبعاد للقاعدة الأفقية. إذاحقيقي ثم تكون القاعدة الأفقية بدون تظليل ثلاثي الأبعاد ويتم استخدام اللون الصلب.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

يشير إلى وجود تظليل ثلاثي الأبعاد للقاعدة الأفقية. إذا`حقيقي`، ثم تكون القاعدة الأفقية بدون تظليل ثلاثي الأبعاد ويتم استخدام اللون الصلب.

```csharp
public bool NoShade { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../horizontalruleformat/)
* المجسم [Aspose.Words](../../../)


