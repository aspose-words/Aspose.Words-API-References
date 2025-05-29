---
title: ThemeFont Enum
linktitle: ThemeFont
articleTitle: ThemeFont
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words ThemeFont enum لإدارة خطوط سمات المستندات بسهولة وتعزيز المظهر المرئي لمستنداتك باستخدام أنماط مخصصة.
type: docs
weight: 7340
url: /ar/net/aspose.words.themes/themefont/
---
## ThemeFont enumeration

يحدد أنواع أسماء خطوط السمات لسمات المستندات.

```csharp
public enum ThemeFont
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يوجد خط موضوعي. |
| Major | `1` | الخط الرئيسي للموضوع. |
| Minor | `2` | خط ذو سمة ثانوية. |

## ملاحظات

يحدد نوع خط السمة الذي يمكن الرجوع إليه كخط سمة ضمن خصائص الكائن الرئيسي. هذا الخط السمة هو مرجع إلى أحد خطوط السمة المحددة مسبقًا، والذي يقع في جزء السمة في المستند، والذي يسمح بتعيين معلومات الخط مركزيًا في المستند.

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
