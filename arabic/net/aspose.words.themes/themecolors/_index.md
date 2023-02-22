---
title: Class ThemeColors
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Themes.ThemeColors فصل. يمثل مخطط ألوان نسق المستند الذي يحتوي على اثني عشر لونًا.
type: docs
weight: 6180
url: /ar/net/aspose.words.themes/themecolors/
---
## ThemeColors class

يمثل مخطط ألوان نسق المستند الذي يحتوي على اثني عشر لونًا.

يحتوي كائن ThemeColors على ستة ألوان تمييز ولونين داكنين ولونين فاتح ولون لكل ارتباط تشعبي ورابط تشعبي متبوع.

```csharp
public class ThemeColors
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | تحديد تمييز اللون 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | تحديد تمييز اللون 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | تحديد تمييز اللون 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | تحديد تمييز اللون 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | تحديد تمييز اللون 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | تحديد تمييز اللون 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | يحدد اللون داكن 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | يحدد اللون الداكن 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | تحديد لون الارتباط التشعبي الذي تم النقر فوقه. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | تحديد لون الارتباط التشعبي . |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | يحدد لون فاتح 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | يحدد لون فاتح 2. |

### أمثلة

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// يتيح لنا كائن "Theme" الوصول إلى سمة المستند ، وهي مصدر للخطوط والألوان الافتراضية.
Theme theme = doc.Theme;

// بعض الأنماط ، مثل "العنوان 1" و "العنوان الفرعي" ، ترث هذه الخطوط.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// قد تحتوي اللغات الأخرى أيضًا على خطوطها المخصصة في هذا الموضوع.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// تحتوي الخاصية "Colors" على لوحة الألوان من Microsoft Word ،
// الذي يظهر عند تغيير التظليل أو لون الخط.
// قم بتطبيق ألوان مخصصة على لوحة الألوان حتى نتمكن من الوصول إليها بسهولة في Microsoft Word
// عندما نقوم ، على سبيل المثال ، بتغيير لون الخط عبر "الصفحة الرئيسية" - >; "الخط" - >. "لون الخط"،
// أو أدخل شكلًا ، ثم قم بتعيين لون له عبر "تنسيق الشكل" - >; "أنماط الشكل".
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

// قم بتطبيق ألوان مخصصة على الارتباطات التشعبية في حالتها التي تم النقر عليها وعدم النقر فوقها.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Themes](../../aspose.words.themes/)
* المجسم [Aspose.Words](../../)


