---
title: HorizontalRuleFormat.Height
second_title: Aspose.Words لمراجع .NET API
description: HorizontalRuleFormat ملكية. الحصول على أو تحديد ارتفاع القاعدة الأفقية.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

الحصول على أو تحديد ارتفاع القاعدة الأفقية.

```csharp
public double Height { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الوسيطة خارج نطاق القيم الصالحة. |

### ملاحظات

هذا اختصار لل[`Height`](../../shapebase/height/) ملكية.

تتراوح القيم الصالحة من 0 إلى 1584 ضمناً.

القيمة الافتراضية هي 1.5.

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


