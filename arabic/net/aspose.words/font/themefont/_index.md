---
title: Font.ThemeFont
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على خط النسق أو تعيينه في نظام الخطوط المطبق المرتبط بكائن الخط هذا.
type: docs
weight: 470
url: /ar/net/aspose.words/font/themefont/
---
## Font.ThemeFont property

الحصول على خط النسق أو تعيينه في نظام الخطوط المطبق المرتبط بكائن الخط هذا.

```csharp
public ThemeFont ThemeFont { get; set; }
```

### أمثلة

يوضح كيفية إنشاء واستخدام نمط ذي موضوع.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// إنشاء نمط بخصائص خط النسق.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

يوضح كيفية العمل مع خطوط وألوان النسق.

```csharp
Document doc = new Document();

// تحديد الخطوط للغات التي تستخدم بشكل افتراضي.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// يمكننا استخدام خط ولون المظهر بدلاً من القيم الافتراضية.
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
// 1 - عن طريق تعيين ThemeFont.None / ThemeColor.None:
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

// 2 - عن طريق تعيين أسماء خطوط / ألوان غير متعلقة بالموضوع:
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

* enum [ThemeFont](../../../aspose.words.themes/themefont/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


