---
title: "ThemeColors"
linktitle: "ThemeColors"
second_title: "Aspose.Words لـ Java"
description: "يمثل مخطط الألوان لسمة المستند التي تحتوي على اثني عشر لونًا في Java."
type: docs
weight: 684
url: /ar/java/com.aspose.words/themecolors/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ThemeColors implements Cloneable
```

يمثل نظام الألوان لسمة المستند الذي يحتوي على اثني عشر لونًا.

[ThemeColors](../../com.aspose.words/themecolors/) object contains six accent colors, two dark colors, two light colors and a color for each of a hyperlink and followed hyperlink.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAccent1()](#getAccent1) | يحدد اللون Accent 1. |
| [getAccent2()](#getAccent2) | يحدد اللون Accent 2. |
| [getAccent3()](#getAccent3) | يحدد اللون Accent 3. |
| [getAccent4()](#getAccent4) | يحدد اللون Accent 4. |
| [getAccent5()](#getAccent5) | يحدد اللون Accent 5. |
| [getAccent6()](#getAccent6) | يحدد اللون Accent 6. |
| [getDark1()](#getDark1) | يحدد اللون Dark 1. |
| [getDark2()](#getDark2) | يحدد اللون Dark 2. |
| [getFollowedHyperlink()](#getFollowedHyperlink) | يحدد اللون لرابط تم النقر عليه. |
| [getHyperlink()](#getHyperlink) | يحدد اللون لرابط. |
| [getLight1()](#getLight1) | يحدد اللون Light 1. |
| [getLight2()](#getLight2) | يحدد اللون Light 2. |
| [setAccent1(Color value)](#setAccent1-java.awt.Color) | يحدد اللون Accent 1. |
| [setAccent2(Color value)](#setAccent2-java.awt.Color) | يحدد اللون Accent 2. |
| [setAccent3(Color value)](#setAccent3-java.awt.Color) | يحدد اللون Accent 3. |
| [setAccent4(Color value)](#setAccent4-java.awt.Color) | يحدد اللون Accent 4. |
| [setAccent5(Color value)](#setAccent5-java.awt.Color) | يحدد اللون Accent 5. |
| [setAccent6(Color value)](#setAccent6-java.awt.Color) | يحدد اللون Accent 6. |
| [setDark1(Color value)](#setDark1-java.awt.Color) | يحدد اللون Dark 1. |
| [setDark2(Color value)](#setDark2-java.awt.Color) | يحدد اللون Dark 2. |
| [setFollowedHyperlink(Color value)](#setFollowedHyperlink-java.awt.Color) | يحدد اللون لرابط تم النقر عليه. |
| [setHyperlink(Color value)](#setHyperlink-java.awt.Color) | يحدد اللون لرابط. |
| [setLight1(Color value)](#setLight1-java.awt.Color) | يحدد اللون Light 1. |
| [setLight2(Color value)](#setLight2-java.awt.Color) | يحدد اللون Light 2. |
### getAccent1() {#getAccent1}
```
public Color getAccent1()
```


يحدد اللون Accent 1.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getAccent2() {#getAccent2}
```
public Color getAccent2()
```


يحدد اللون Accent 2.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getAccent3() {#getAccent3}
```
public Color getAccent3()
```


يحدد اللون Accent 3.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getAccent4() {#getAccent4}
```
public Color getAccent4()
```


يحدد اللون Accent 4.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getAccent5() {#getAccent5}
```
public Color getAccent5()
```


يحدد اللون Accent 5.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getAccent6() {#getAccent6}
```
public Color getAccent6()
```


يحدد اللون Accent 6.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getDark1() {#getDark1}
```
public Color getDark1()
```


يحدد اللون Dark 1.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getDark2() {#getDark2}
```
public Color getDark2()
```


يحدد اللون Dark 2.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getFollowedHyperlink() {#getFollowedHyperlink}
```
public Color getFollowedHyperlink()
```


يحدد اللون لرابط تم النقر عليه.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getHyperlink() {#getHyperlink}
```
public Color getHyperlink()
```


يحدد اللون لرابط.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getLight1() {#getLight1}
```
public Color getLight1()
```


يحدد اللون Light 1.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### getLight2() {#getLight2}
```
public Color getLight2()
```


يحدد اللون Light 2.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
java.awt.Color - القيمة المقابلة لـ java.awt.Color.
### setAccent1(Color value) {#setAccent1-java.awt.Color}
```
public void setAccent1(Color value)
```


يحدد اللون Accent 1.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setAccent2(Color value) {#setAccent2-java.awt.Color}
```
public void setAccent2(Color value)
```


يحدد اللون Accent 2.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setAccent3(Color value) {#setAccent3-java.awt.Color}
```
public void setAccent3(Color value)
```


يحدد اللون Accent 3.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setAccent4(Color value) {#setAccent4-java.awt.Color}
```
public void setAccent4(Color value)
```


يحدد اللون Accent 4.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setAccent5(Color value) {#setAccent5-java.awt.Color}
```
public void setAccent5(Color value)
```


يحدد اللون Accent 5.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setAccent6(Color value) {#setAccent6-java.awt.Color}
```
public void setAccent6(Color value)
```


يحدد اللون Accent 6.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setDark1(Color value) {#setDark1-java.awt.Color}
```
public void setDark1(Color value)
```


يحدد اللون Dark 1.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setDark2(Color value) {#setDark2-java.awt.Color}
```
public void setDark2(Color value)
```


يحدد اللون Dark 2.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setFollowedHyperlink(Color value) {#setFollowedHyperlink-java.awt.Color}
```
public void setFollowedHyperlink(Color value)
```


يحدد اللون لرابط تم النقر عليه.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setHyperlink(Color value) {#setHyperlink-java.awt.Color}
```
public void setHyperlink(Color value)
```


يحدد اللون لرابط.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setLight1(Color value) {#setLight1-java.awt.Color}
```
public void setLight1(Color value)
```


يحدد اللون Light 1.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

### setLight2(Color value) {#setLight2-java.awt.Color}
```
public void setLight2(Color value)
```


يحدد اللون Light 2.

 **Examples:** 

يوضح كيفية تعيين ألوان وخطوط مخصصة للسمات.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | القيمة المقابلة لـ java.awt.Color. |

