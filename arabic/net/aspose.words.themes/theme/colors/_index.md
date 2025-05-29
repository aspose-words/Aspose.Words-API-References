---
title: Theme.Colors
linktitle: Colors
articleTitle: Colors
second_title: Aspose.Words لـ .NET
description: قم بتخصيص مظهر مستندك باستخدام خاصية ألوان السمة، مما يتيح لك الحصول على مجموعة فريدة من الألوان النابضة بالحياة للحصول على مظهر مذهل.
type: docs
weight: 20
url: /ar/net/aspose.words.themes/theme/colors/
---
## Theme.Colors property

يسمح بتحديد مجموعة ألوان السمة للمستند.

```csharp
public ThemeColors Colors { get; }
```

## أمثلة

يوضح كيفية تعيين الألوان والخطوط المخصصة للموضوعات.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// يمنحنا كائن "المظهر" إمكانية الوصول إلى مظهر المستند، وهو مصدر الخطوط والألوان الافتراضية.
Theme theme = doc.Theme;

// بعض الأنماط، مثل "العنوان 1" و"العنوان الفرعي"، سوف ترث هذه الخطوط.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// قد يكون للغات الأخرى أيضًا خطوطها المخصصة في هذا المظهر.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// تحتوي خاصية "الألوان" على لوحة الألوان من Microsoft Word،
//الذي يظهر عند تغيير التظليل أو لون الخط.
// تطبيق ألوان مخصصة على لوحة الألوان حتى نتمكن من الوصول إليها بسهولة في Microsoft Word
// عندما نقوم، على سبيل المثال، بتغيير لون الخط عبر "الصفحة الرئيسية" -> "الخط" -> "لون الخط"،
// أو أدخل شكلًا، ثم قم بتعيين لون له عبر "تنسيق الشكل" -> "أنماط الشكل".
ThemeColors colors = theme.Colors;
colors.Dark1 = Color.MidnightBlue;
colors.Light1 = Color.PaleGreen;
colors.Dark2 = Color.Indigo;
colors.Light2 = Color.Khaki;

colors.Accent1 = Color.OrangeRed;
colors.Accent2 = Color.LightSalmon;
colors.Accent3 = Color.Yellow;
colors.Accent4 = Color.Gold;
colors.Accent5 = Color.BlueViolet;
colors.Accent6 = Color.DarkViolet;

// تطبيق الألوان المخصصة على الروابط التشعبية في حالتها عند النقر عليها أو عدم النقر عليها.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### أنظر أيضا

* class [ThemeColors](../../themecolors/)
* class [Theme](../)
* مساحة الاسم [Aspose.Words.Themes](../../../aspose.words.themes/)
* المجسم [Aspose.Words](../../../)
