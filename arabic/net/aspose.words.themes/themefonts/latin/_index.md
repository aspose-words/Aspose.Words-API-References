---
title: ThemeFonts.Latin
linktitle: Latin
articleTitle: Latin
second_title: Aspose.Words لـ .NET
description: اكتشف ThemeFonts للحروف اللاتينية! حسّن تصميمك بخيارات خطوط قابلة للتخصيص تُحسّن أسلوب الطباعة وتجربة المستخدم.
type: docs
weight: 30
url: /ar/net/aspose.words.themes/themefonts/latin/
---
## ThemeFonts.Latin property

يحدد اسم الخط للأحرف اللاتينية.

```csharp
public string Latin { get; set; }
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

* class [ThemeFonts](../)
* مساحة الاسم [Aspose.Words.Themes](../../../aspose.words.themes/)
* المجسم [Aspose.Words](../../../)
