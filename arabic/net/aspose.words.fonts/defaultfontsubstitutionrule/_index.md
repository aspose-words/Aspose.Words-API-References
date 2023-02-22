---
title: Class DefaultFontSubstitutionRule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule فصل. قاعدة استبدال الخط الافتراضي.
type: docs
weight: 2660
url: /ar/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

قاعدة استبدال الخط الافتراضي.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | الحصول على اسم الخط الافتراضي أو تعيينه. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | يحدد ما إذا كانت القاعدة ممكّنة أم لا. |

### ملاحظات

تحدد هذه القاعدة اسم الخط الافتراضي الفردي الذي سيتم استخدامه للاستبدال في حالة عدم توفر الخط الأصلي.

### أمثلة

يوضح كيفية تعيين قاعدة استبدال الخط الافتراضي.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// احصل على قاعدة الاستبدال الافتراضية داخل FontSettings.
// ستستبدل هذه القاعدة جميع الخطوط المفقودة بـ "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// قم بتعيين بديل الخط الافتراضي على "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// باستخدام مُنشئ المستندات ، أضف بعض النص بخط لسنا مضطرين لرؤية الاستبدال ،
// ثم اعرض النتيجة في ملف PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### أنظر أيضا

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)


