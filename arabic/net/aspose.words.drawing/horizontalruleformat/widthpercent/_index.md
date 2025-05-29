---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HorizontalRuleFormat WidthPercent لتخصيص طول القاعدة الأفقية بسهولة كنسبة مئوية من عرض النافذة للتحكم في التصميم بشكل أفضل.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

يحصل على طول القاعدة الأفقية المحددة أو يعينه معبرًا عنها كنسبة مئوية من عرض النافذة.

```csharp
public double WidthPercent { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الحجة خارج نطاق القيم الصالحة. |

## ملاحظات

تتراوح القيم الصالحة من 1 إلى 100 شاملة.

القيمة الافتراضية هي 100.

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
