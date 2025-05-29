---
title: HorizontalRuleFormat.NoShade
linktitle: NoShade
articleTitle: NoShade
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HorizontalRuleFormat NoShade، وتحكم في التظليل ثلاثي الأبعاد للقواعد الأفقية. احصل على تصميم أنيق بلون واحد بكل سهولة!
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

يشير إلى وجود تظليل ثلاثي الأبعاد للمسطرة الأفقية. إذا`حقيقي` ، ثم تكون القاعدة الأفقية بدون تظليل ثلاثي الأبعاد ويتم استخدام اللون الصلب.

```csharp
public bool NoShade { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

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
