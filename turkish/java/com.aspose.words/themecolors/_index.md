---
title: "ThemeColors"
linktitle: "ThemeColors"
second_title: "Aspose.Words Java için"
description: "Java'da on iki renk içeren belge temasının renk şemasını temsil eder."
type: docs
weight: 684
url: /tr/java/com.aspose.words/themecolors/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ThemeColors implements Cloneable
```

On iki renk içeren belge temasının renk şemasını temsil eder.

[ThemeColors](../../com.aspose.words/themecolors/) object contains six accent colors, two dark colors, two light colors and a color for each of a hyperlink and followed hyperlink.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAccent1()](#getAccent1) | Accent 1 rengini belirtir. |
| [getAccent2()](#getAccent2) | Accent 2 rengini belirtir. |
| [getAccent3()](#getAccent3) | Accent 3 rengini belirtir. |
| [getAccent4()](#getAccent4) | Accent 4 rengini belirtir. |
| [getAccent5()](#getAccent5) | Accent 5 rengini belirtir. |
| [getAccent6()](#getAccent6) | Accent 6 rengini belirtir. |
| [getDark1()](#getDark1) | Dark 1 rengini belirtir. |
| [getDark2()](#getDark2) | Dark 2 rengini belirtir. |
| [getFollowedHyperlink()](#getFollowedHyperlink) | Tıklanmış bir bağlantı için rengi belirtir. |
| [getHyperlink()](#getHyperlink) | Bir bağlantı için rengi belirtir. |
| [getLight1()](#getLight1) | Light 1 rengini belirtir. |
| [getLight2()](#getLight2) | Light 2 rengini belirtir. |
| [setAccent1(Color value)](#setAccent1-java.awt.Color) | Accent 1 rengini belirtir. |
| [setAccent2(Color value)](#setAccent2-java.awt.Color) | Accent 2 rengini belirtir. |
| [setAccent3(Color value)](#setAccent3-java.awt.Color) | Accent 3 rengini belirtir. |
| [setAccent4(Color value)](#setAccent4-java.awt.Color) | Accent 4 rengini belirtir. |
| [setAccent5(Color value)](#setAccent5-java.awt.Color) | Accent 5 rengini belirtir. |
| [setAccent6(Color value)](#setAccent6-java.awt.Color) | Accent 6 rengini belirtir. |
| [setDark1(Color value)](#setDark1-java.awt.Color) | Dark 1 rengini belirtir. |
| [setDark2(Color value)](#setDark2-java.awt.Color) | Dark 2 rengini belirtir. |
| [setFollowedHyperlink(Color value)](#setFollowedHyperlink-java.awt.Color) | Tıklanmış bir bağlantı için rengi belirtir. |
| [setHyperlink(Color value)](#setHyperlink-java.awt.Color) | Bir bağlantı için rengi belirtir. |
| [setLight1(Color value)](#setLight1-java.awt.Color) | Light 1 rengini belirtir. |
| [setLight2(Color value)](#setLight2-java.awt.Color) | Light 2 rengini belirtir. |
### getAccent1() {#getAccent1}
```
public Color getAccent1()
```


Accent 1 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getAccent2() {#getAccent2}
```
public Color getAccent2()
```


Accent 2 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getAccent3() {#getAccent3}
```
public Color getAccent3()
```


Accent 3 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getAccent4() {#getAccent4}
```
public Color getAccent4()
```


Accent 4 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getAccent5() {#getAccent5}
```
public Color getAccent5()
```


Accent 5 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getAccent6() {#getAccent6}
```
public Color getAccent6()
```


Accent 6 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getDark1() {#getDark1}
```
public Color getDark1()
```


Dark 1 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getDark2() {#getDark2}
```
public Color getDark2()
```


Dark 2 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getFollowedHyperlink() {#getFollowedHyperlink}
```
public Color getFollowedHyperlink()
```


Tıklanmış bir bağlantı için rengi belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getHyperlink() {#getHyperlink}
```
public Color getHyperlink()
```


Bir bağlantı için rengi belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getLight1() {#getLight1}
```
public Color getLight1()
```


Light 1 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### getLight2() {#getLight2}
```
public Color getLight2()
```


Light 2 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
java.awt.Color - İlgili java.awt.Color değeri.
### setAccent1(Color value) {#setAccent1-java.awt.Color}
```
public void setAccent1(Color value)
```


Accent 1 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setAccent2(Color value) {#setAccent2-java.awt.Color}
```
public void setAccent2(Color value)
```


Accent 2 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setAccent3(Color value) {#setAccent3-java.awt.Color}
```
public void setAccent3(Color value)
```


Accent 3 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setAccent4(Color value) {#setAccent4-java.awt.Color}
```
public void setAccent4(Color value)
```


Accent 4 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setAccent5(Color value) {#setAccent5-java.awt.Color}
```
public void setAccent5(Color value)
```


Accent 5 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setAccent6(Color value) {#setAccent6-java.awt.Color}
```
public void setAccent6(Color value)
```


Accent 6 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setDark1(Color value) {#setDark1-java.awt.Color}
```
public void setDark1(Color value)
```


Dark 1 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setDark2(Color value) {#setDark2-java.awt.Color}
```
public void setDark2(Color value)
```


Dark 2 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setFollowedHyperlink(Color value) {#setFollowedHyperlink-java.awt.Color}
```
public void setFollowedHyperlink(Color value)
```


Tıklanmış bir bağlantı için rengi belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setHyperlink(Color value) {#setHyperlink-java.awt.Color}
```
public void setHyperlink(Color value)
```


Bir bağlantı için rengi belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setLight1(Color value) {#setLight1-java.awt.Color}
```
public void setLight1(Color value)
```


Light 1 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

### setLight2(Color value) {#setLight2-java.awt.Color}
```
public void setLight2(Color value)
```


Light 2 rengini belirtir.

 **Examples:** 

Temalar için özel renkler ve yazı tipleri nasıl ayarlanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | İlgili java.awt.Color değeri. |

