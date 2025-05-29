---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.DefaultFontSubstitutionRule لإدارة الخطوط بسلاسة وتنسيق المستندات بشكل مُحسّن. حسّن سير عملك اليوم!
type: docs
weight: 3250
url: /ar/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

قاعدة استبدال الخط الافتراضية.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | يحصل على اسم الخط الافتراضي أو يعينه. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | يحدد ما إذا كانت القاعدة ممكّنة أم لا. |

## ملاحظات

تحدد هذه القاعدة اسم الخط الافتراضي الوحيد الذي سيتم استخدامه للاستبدال إذا لم يكن الخط الأصلي متاحًا.

## أمثلة

يوضح كيفية تعيين قاعدة استبدال الخط الافتراضية.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// احصل على قاعدة الاستبدال الافتراضية ضمن FontSettings.
// ستقوم هذه القاعدة باستبدال جميع الخطوط المفقودة بـ "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// تعيين الخط البديل الافتراضي إلى "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// باستخدام منشئ المستندات، أضف بعض النصوص بخط لا نحتاج إليه لرؤية عملية الاستبدال،
// ثم قم بعرض النتيجة في ملف PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### أنظر أيضا

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
