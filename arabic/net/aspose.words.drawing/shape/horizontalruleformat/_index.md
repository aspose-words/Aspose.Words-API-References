---
title: Shape.HorizontalRuleFormat
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words لـ .NET
description: Shape HorizontalRuleFormat ملكية. يوفر الوصول إلى خصائص شكل القاعدة الأفقية. بالنسبة للشكل الذي لا يمثل قاعدة أفقية يتم إرجاعهباطل  في C#.
type: docs
weight: 100
url: /ar/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

يوفر الوصول إلى خصائص شكل القاعدة الأفقية. بالنسبة للشكل الذي لا يمثل قاعدة أفقية، يتم إرجاعه`باطل` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
