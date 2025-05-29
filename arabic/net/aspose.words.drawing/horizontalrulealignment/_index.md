---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.HorizontalRuleAlignment للتحكم الدقيق في محاذاة القاعدة الأفقية، مما يعزز تنسيق مستندك وتصميمه.
type: docs
weight: 1370
url: /ar/net/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enumeration

يمثل محاذاة القاعدة الأفقية المحددة.

```csharp
public enum HorizontalRuleAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Left | `0` | محاذي لليسار. |
| Center | `1` | محاذية للمركز. |
| Right | `2` | محاذي لليمين. |

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
