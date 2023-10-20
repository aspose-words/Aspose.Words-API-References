---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Settings.HyphenationOptions فصل. يسمح بتكوين خيارات الواصلة للمستند في C#.
type: docs
weight: 5790
url: /ar/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

يسمح بتكوين خيارات الواصلة للمستند.

لمعرفة المزيد، قم بزيارة[العمل مع الواصلة](https://docs.aspose.com/words/net/working-with-hyphenation/) مقالة توثيقية.

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
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم تشغيل الواصلة التلقائية للمستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | الحصول على أو تعيين الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بواصلات. القيمة الافتراضية لهذه الخاصية هي 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة موصولة بواصلة. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | الحصول على أو تعيين المسافة بـ 1/20 نقطة من الهامش الأيمن الذي لا تريد وصل الكلمات فيه. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة). |

## أمثلة

يوضح كيفية تكوين الواصلة التلقائية.

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
