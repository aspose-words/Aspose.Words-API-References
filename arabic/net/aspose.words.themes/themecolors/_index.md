---
title: ThemeColors Class
linktitle: ThemeColors
articleTitle: ThemeColors
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.ThemeColors، التي تتميز بمخطط ألوان متعدد الاستخدامات مكون من 12 لونًا لتعزيز الجاذبية البصرية والمتناسقة لمستندك.
type: docs
weight: 7330
url: /ar/net/aspose.words.themes/themecolors/
---
## ThemeColors class

يمثل مخطط الألوان لموضوع المستند والذي يحتوي على اثني عشر لونًا.

`ThemeColors` يحتوي الكائن على ستة ألوان مميزة، لونين داكنين، لونين فاتحين ولون لكل من الارتباط التشعبي والارتباط التشعبي التالي.

```csharp
public class ThemeColors
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | يحدد لون Accent 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | يحدد لون Accent 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | يحدد لون Accent 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | يحدد لون Accent 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | يحدد لون Accent 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | يحدد لون Accent 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | يحدد اللون الداكن 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | يحدد اللون الداكن 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | يحدد اللون للرابط التشعبي الذي تم النقر عليه. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | يحدد اللون للارتباط التشعبي. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | يحدد لون الضوء 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | يحدد لون الضوء 2. |

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

* مساحة الاسم [Aspose.Words.Themes](../../aspose.words.themes/)
* المجسم [Aspose.Words](../../)
