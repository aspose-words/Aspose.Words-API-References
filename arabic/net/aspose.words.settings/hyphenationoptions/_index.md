---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Settings.HyphenationOptions لتخصيص إعدادات الوصل بسهولة لمستنداتك وتحسين عرض النص.
type: docs
weight: 6620
url: /ar/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

يسمح بتكوين خيارات وضع علامات الوصل في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الوصلات](https://docs.aspose.com/words/net/working-with-hyphenation/) مقالة توثيقية.

```csharp
public class HyphenationOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | يحصل على القيمة أو يعينها لتحديد ما إذا كان يتم تشغيل الوصل التلقائي للمستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | يحصل على أو يعين الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بواصلات. القيمة الافتراضية لهذه الخاصية هي 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | يحصل على القيمة أو يعينها لتحديد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة جميعها موصولة بواصلة. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | يحصل على أو يضبط المسافة بمقدار 1/20 من نقطة من الهامش الأيمن الذي لا تريد أن تقوم بوضع علامة وصل بين الكلمات فيه. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة). |

## أمثلة

يوضح كيفية تكوين الوصلة التلقائية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
