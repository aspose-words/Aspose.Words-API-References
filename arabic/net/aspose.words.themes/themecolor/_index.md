---
title: ThemeColor Enum
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Themes.ThemeColor تعداد. تحديد ألوان السمات لموضوعات المستند في C#.
type: docs
weight: 6470
url: /ar/net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

تحديد ألوان السمات لموضوعات المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأنماط والموضوعات](https://docs.aspose.com/words/net/working-with-styles-and-themes/) مقالة توثيقية.

```csharp
public enum ThemeColor
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `-1` | بلا لون. |
| Dark1 | `0` | اللون الرئيسي الداكن 1. |
| Light1 | `1` | اللون الرئيسي الفاتح 1. |
| Dark2 | `2` | اللون الرئيسي الداكن 2. |
| Light2 | `3` | اللون الرئيسي الفاتح 2. |
| Accent1 | `4` | اللون المميز 1. |
| Accent2 | `5` | اللون المميز 2. |
| Accent3 | `6` | اللون المميز 3. |
| Accent4 | `7` | اللون المميز 4. |
| Accent5 | `8` | اللون المميز 5. |
| Accent6 | `9` | اللون المميز 6. |
| Hyperlink | `10` | لون الارتباط التشعبي. |
| FollowedHyperlink | `11` | لون الارتباط التشعبي المتبع. |
| Text1 | `12` | لون النص 1. |
| Text2 | `13` | لون النص 2. |
| Background1 | `14` | لون الخلفية 1. |
| Background2 | `15` | لون الخلفية 2. |

## ملاحظات

لون السمة المحدد هو مرجع لأحد ألوان السمة المحددة مسبقًا، والموجود في جزء السمة الخاص بالمستند ، والذي يسمح بتعيين معلومات اللون مركزيًا في المستند.

## أمثلة

يوضح كيفية إنشاء واستخدام النمط الموضوعي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// قم بإنشاء نمط ما باستخدام خصائص خط السمة.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

يوضح كيفية العمل مع خطوط وألوان السمات.

```csharp
Document doc = new Document();

// تحديد الخطوط لاستخدامات اللغات بشكل افتراضي.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// يمكننا استخدام خط السمة ولونها بدلاً من القيم الافتراضية.
font.ThemeFont = ThemeFont.Minor;
font.ThemeColor = ThemeColor.Accent2;

Assert.AreEqual(ThemeFont.Minor, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.Accent2, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// هناك عدة طرق لإعادة ضبط الخط واللون.
// 1 - عن طريق ضبط ThemeFont.None/ThemeColor.None:
font.ThemeFont = ThemeFont.None;
font.ThemeColor = ThemeColor.None;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// 2 - عن طريق تعيين أسماء الخطوط/الألوان غير الموضوعية:
font.Name = "Arial";
font.Color = Color.Blue;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Arial", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Arial", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Arial", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Arial", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Arial", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Blue.ToArgb(), font.Color.ToArgb());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Themes](../../aspose.words.themes/)
* المجسم [Aspose.Words](../../)
