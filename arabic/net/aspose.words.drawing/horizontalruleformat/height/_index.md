---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words لـ .NET
description: اضبط ارتفاع مسطرتك الأفقية بسهولة. استكشف خاصية الارتفاع لتصميم قابل للتخصيص في مشاريع الويب الخاصة بك. حسّن تصميمك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

يحصل على ارتفاع المسطرة الأفقية أو يعينه.

```csharp
public double Height { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الحجة خارج نطاق القيم الصالحة. |

## ملاحظات

هذا اختصار لـ[`Height`](../../shapebase/height/) ملكية.

تتراوح القيم الصالحة من 0 إلى 1584 شاملة.

القيمة الافتراضية هي 1.5.

## أمثلة

يوضح كيفية إدراج شكل مسطرة أفقية وتخصيص تنسيقها.

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
