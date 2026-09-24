---
title: "Tema"
linktitle: "Tema"
second_title: "Aspose.Words Java için"
description: "Belge temasını temsil eder ve Java'da getMajorFonts, getMinorFonts ve getColors dahil olmak üzere ana tema bölümlerine erişim sağlar."
type: docs
weight: 682
url: /tr/java/com.aspose.words/theme/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Theme implements Cloneable
```

Belge temasını temsil eder ve [getMajorFonts()](../../com.aspose.words/theme/\#getMajorFonts), [getMinorFonts()](../../com.aspose.words/theme/\#getMinorFonts) ve [getColors()](../../com.aspose.words/theme/\#getColors) dahil olmak üzere ana tema bölümlerine erişim sağlar.

Daha fazla bilgi için, [ Working with Styles and Themes ][Working with Styles and Themes] dokümantasyon makalesini ziyaret edin.

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


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getColors()](#getColors) | Belge için tema renkleri kümesini belirtmeye olanak tanır. |
| [getFontName(int themeFont)](#getFontName-int) |  |
| [getMajorFonts()](#getMajorFonts) | Farklı diller için ana yazı tipleri kümesini belirtmeye olanak tanır. |
| [getMinorFonts()](#getMinorFonts) | Farklı diller için yan yazı tipleri kümesini belirtmeye olanak tanır. |
| [onChange()](#onChange) |  |
### getColors() {#getColors}
```
public ThemeColors getColors()
```


Belge için tema renkleri kümesini belirtmeye olanak tanır.

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
[ThemeColors](../../com.aspose.words/themecolors/) - The corresponding [ThemeColors](../../com.aspose.words/themecolors/) value.
### getFontName(int themeFont) {#getFontName-int}
```
public String getFontName(int themeFont)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| themeFont | int |  |

**Returns:**
java.lang.String
### getMajorFonts() {#getMajorFonts}
```
public ThemeFonts getMajorFonts()
```


Farklı diller için ana yazı tipleri kümesini belirtmeye olanak tanır.

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
[ThemeFonts](../../com.aspose.words/themefonts/) - The corresponding [ThemeFonts](../../com.aspose.words/themefonts/) value.
### getMinorFonts() {#getMinorFonts}
```
public ThemeFonts getMinorFonts()
```


Farklı diller için yan yazı tipleri kümesini belirtmeye olanak tanır.

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
[ThemeFonts](../../com.aspose.words/themefonts/) - The corresponding [ThemeFonts](../../com.aspose.words/themefonts/) value.
### onChange() {#onChange}
```
public void onChange()
```




