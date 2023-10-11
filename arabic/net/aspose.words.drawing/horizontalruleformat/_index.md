---
title: Class HorizontalRuleFormat
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.HorizontalRuleFormat فصل. يمثل تنسيق القاعدة الأفقي.
type: docs
weight: 1050
url: /ar/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

يمثل تنسيق القاعدة الأفقي.

لمعرفة المزيد، قم بزيارة[العمل مع الأشكال](https://docs.aspose.com/words/net/working-with-shapes/) مقالة توثيقية.

```csharp
public class HorizontalRuleFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | الحصول على أو تعيين محاذاة القاعدة الأفقية. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | الحصول على أو تعيين لون الفرشاة الذي يملأ القاعدة الأفقية. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | الحصول على أو تحديد ارتفاع القاعدة الأفقية. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | يشير إلى وجود تظليل ثلاثي الأبعاد للقاعدة الأفقية. إذا`حقيقي`، ثم تكون القاعدة الأفقية بدون تظليل ثلاثي الأبعاد ويتم استخدام اللون الصلب. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | الحصول على أو تعيين طول القاعدة الأفقية المحددة معبرًا عنها كنسبة مئوية من عرض النافذة. |

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


