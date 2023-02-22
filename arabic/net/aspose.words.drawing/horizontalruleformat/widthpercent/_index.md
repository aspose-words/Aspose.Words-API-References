---
title: HorizontalRuleFormat.WidthPercent
second_title: Aspose.Words لمراجع .NET API
description: HorizontalRuleFormat ملكية. الحصول على أو تحديد طول القاعدة الأفقية المحددة كنسبة مئوية من عرض النافذة.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

الحصول على أو تحديد طول القاعدة الأفقية المحددة كنسبة مئوية من عرض النافذة.

```csharp
public double WidthPercent { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يظهر عندما تكون الوسيطة خارج نطاق القيم الصالحة. |

### ملاحظات

تتراوح القيم الصالحة من 1 إلى 100 ضمناً.

القيمة الافتراضية هي 100.

### أمثلة

يوضح كيفية إدراج شكل تسطير أفقي ، وتخصيص تنسيقه.

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


