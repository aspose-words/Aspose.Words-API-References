---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية لون HorizontalRuleFormat لتخصيص تصميمك. اضبط أو احصل على لون الفرشاة بسهولة للحصول على تأثير خط أفقي مذهل!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

يحصل على لون الفرشاة التي تملأ الخط الأفقي أو يعينه.

```csharp
public Color Color { get; set; }
```

## ملاحظات

هذا اختصار لـ[`Color`](../../fill/color/) ملكية.

القيمة الافتراضية هي Gray .

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
