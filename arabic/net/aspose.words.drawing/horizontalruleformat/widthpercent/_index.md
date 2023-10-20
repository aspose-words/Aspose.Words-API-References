---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: Aspose.Words لـ .NET
description: HorizontalRuleFormat WidthPercent ملكية. الحصول على أو تعيين طول القاعدة الأفقية المحددة معبرًا عنها كنسبة مئوية من عرض النافذة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

الحصول على أو تعيين طول القاعدة الأفقية المحددة معبرًا عنها كنسبة مئوية من عرض النافذة.

```csharp
public double WidthPercent { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم طرحه عندما تكون الوسيطة خارج نطاق القيم الصالحة. |

## ملاحظات

تتراوح القيم الصالحة من 1 إلى 100 ضمناً.

القيمة الافتراضية هي 100.

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
