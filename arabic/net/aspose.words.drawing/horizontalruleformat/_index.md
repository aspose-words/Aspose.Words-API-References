---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.HorizontalRuleFormat لتنسيق الخطوط الأفقية المتقدمة. حسّن تصميم مستندك بسهولة!
type: docs
weight: 1380
url: /ar/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

يمثل تنسيق القاعدة الأفقية.

لمعرفة المزيد، قم بزيارة[العمل مع الأشكال](https://docs.aspose.com/words/net/working-with-shapes/) مقالة توثيقية.

```csharp
public class HorizontalRuleFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | يحصل على محاذاة القاعدة الأفقية أو يعينها. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | يحصل على لون الفرشاة التي تملأ الخط الأفقي أو يعينه. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | يحصل على ارتفاع المسطرة الأفقية أو يعينه. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | يشير إلى وجود تظليل ثلاثي الأبعاد للمسطرة الأفقية. إذا`حقيقي` ، ثم تكون القاعدة الأفقية بدون تظليل ثلاثي الأبعاد ويتم استخدام اللون الصلب. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | يحصل على طول القاعدة الأفقية المحددة أو يعينه معبرًا عنها كنسبة مئوية من عرض النافذة. |

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
