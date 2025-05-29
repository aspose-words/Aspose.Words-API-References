---
title: ThemeColor Enum
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words ThemeColor لتخصيص سمات المستندات بألوان نابضة بالحياة، مما يعزز الجاذبية البصرية لمستندك واحترافيته.
type: docs
weight: 7320
url: /ar/net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

يحدد ألوان السمة لسمات المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأنماط والموضوعات](https://docs.aspose.com/words/net/working-with-styles-and-themes/) مقالة توثيقية.

```csharp
public enum ThemeColor
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `-1` | بدون لون. |
| Dark1 | `0` | اللون الرئيسي الداكن 1. |
| Light1 | `1` | اللون الرئيسي للضوء 1. |
| Dark2 | `2` | اللون الرئيسي الداكن 2. |
| Light2 | `3` | اللون الرئيسي للضوء 2. |
| Accent1 | `4` | لون مميز 1. |
| Accent2 | `5` | لون مميز 2. |
| Accent3 | `6` | لون مميز 3. |
| Accent4 | `7` | لون مميز 4. |
| Accent5 | `8` | لون مميز 5. |
| Accent6 | `9` | لون مميز 6. |
| Hyperlink | `10` | لون الارتباط التشعبي. |
| FollowedHyperlink | `11` | لون الرابط التشعبي المتبع. |
| Text1 | `12` | لون النص 1. |
| Text2 | `13` | لون النص 2. |
| Background1 | `14` | لون الخلفية 1. |
| Background2 | `15` | لون الخلفية 2. |

## ملاحظات

لون السمة المحدد هو إشارة إلى أحد ألوان السمة المحددة مسبقًا، والتي توجد في جزء السمة في مستند ، والذي يسمح بتعيين معلومات اللون مركزيًا في المستند.

## أمثلة

يوضح كيفية إنشاء النمط الموضوعي واستخدامه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// قم بإنشاء بعض الأنماط باستخدام خصائص الخط الخاص بالموضوع.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

يوضح كيفية العمل مع الخطوط والألوان الخاصة بالموضوع.

```csharp
Document doc = new Document();

// قم بتحديد الخطوط لاستخدامات اللغات بشكل افتراضي.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

//يمكننا استخدام الخط واللون الخاص بالموضوع بدلاً من القيم الافتراضية.
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

// هناك عدة طرق لإعادة تعيين الخط واللون.
// 1 - عن طريق تعيين ThemeFont.None/ThemeColor.None:
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

// 2 - عن طريق تعيين أسماء الخطوط/الألوان غير المتعلقة بالموضوع:
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
