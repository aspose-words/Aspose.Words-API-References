---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية "استبدال الخط الافتراضي" إعدادات الخط لضمان طباعة سلسة. حسّن تصميمك بقواعد استبدال خطوط فعّالة.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

الإعدادات المتعلقة بقاعدة استبدال الخط الافتراضي.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

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

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
