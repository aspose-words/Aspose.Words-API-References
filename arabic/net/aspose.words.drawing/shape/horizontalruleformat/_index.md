---
title: Shape.HorizontalRuleFormat
second_title: Aspose.Words لمراجع .NET API
description: Shape ملكية. يوفر الوصول إلى خصائص شكل القاعدة الأفقية. بالنسبة للشكل الذي ليس قاعدة أفقية  يتم إرجاع قيمة خالية.
type: docs
weight: 100
url: /ar/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

يوفر الوصول إلى خصائص شكل القاعدة الأفقية. بالنسبة للشكل الذي ليس قاعدة أفقية ، يتم إرجاع قيمة خالية.

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shape/)
* المجسم [Aspose.Words](../../../)


