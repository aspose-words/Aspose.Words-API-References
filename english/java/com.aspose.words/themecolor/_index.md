---
title: ThemeColor
linktitle: ThemeColor
second_title: Aspose.Words for Java
description: Specifies the theme colors for document themes in Java.
type: docs
weight: 634
url: /java/com.aspose.words/themecolor/
---

**Inheritance:**
java.lang.Object
```
public class ThemeColor
```

Specifies the theme colors for document themes.

To learn more, visit the [ Working with Styles and Themes ][Working with Styles and Themes] documentation article.

 **Remarks:** 

The specified theme color is a reference to one of the predefined theme colors, located in the document's Theme part, which allows color information to be set centrally in the document.

 **Examples:** 

Shows how to create and use themed style.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

Shows how to work with theme fonts and colors.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## Fields

| Field | Description |
| --- | --- |
| [ACCENT_1](#ACCENT-1) | Accent color 1. |
| [ACCENT_2](#ACCENT-2) | Accent color 2. |
| [ACCENT_3](#ACCENT-3) | Accent color 3. |
| [ACCENT_4](#ACCENT-4) | Accent color 4. |
| [ACCENT_5](#ACCENT-5) | Accent color 5. |
| [ACCENT_6](#ACCENT-6) | Accent color 6. |
| [BACKGROUND_1](#BACKGROUND-1) | Background color 1. |
| [BACKGROUND_2](#BACKGROUND-2) | Background color 2. |
| [DARK_1](#DARK-1) | Dark main color 1. |
| [DARK_2](#DARK-2) | Dark main color 2. |
| [FOLLOWED_HYPERLINK](#FOLLOWED-HYPERLINK) | Followed hyperlink color. |
| [HYPERLINK](#HYPERLINK) | Hyperlink color. |
| [LIGHT_1](#LIGHT-1) | Light main color 1. |
| [LIGHT_2](#LIGHT-2) | Light main color 2. |
| [NONE](#NONE) | No color. |
| [TEXT_1](#TEXT-1) | Text color 1. |
| [TEXT_2](#TEXT-2) | Text color 2. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String themeColorName)](#fromName-java.lang.String) |  |
| [getName(int themeColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int themeColor)](#toString-int) |  |
### ACCENT_1 {#ACCENT-1}
```
public static int ACCENT_1
```


Accent color 1.

### ACCENT_2 {#ACCENT-2}
```
public static int ACCENT_2
```


Accent color 2.

### ACCENT_3 {#ACCENT-3}
```
public static int ACCENT_3
```


Accent color 3.

### ACCENT_4 {#ACCENT-4}
```
public static int ACCENT_4
```


Accent color 4.

### ACCENT_5 {#ACCENT-5}
```
public static int ACCENT_5
```


Accent color 5.

### ACCENT_6 {#ACCENT-6}
```
public static int ACCENT_6
```


Accent color 6.

### BACKGROUND_1 {#BACKGROUND-1}
```
public static int BACKGROUND_1
```


Background color 1.

### BACKGROUND_2 {#BACKGROUND-2}
```
public static int BACKGROUND_2
```


Background color 2.

### DARK_1 {#DARK-1}
```
public static int DARK_1
```


Dark main color 1.

### DARK_2 {#DARK-2}
```
public static int DARK_2
```


Dark main color 2.

### FOLLOWED_HYPERLINK {#FOLLOWED-HYPERLINK}
```
public static int FOLLOWED_HYPERLINK
```


Followed hyperlink color.

### HYPERLINK {#HYPERLINK}
```
public static int HYPERLINK
```


Hyperlink color.

### LIGHT_1 {#LIGHT-1}
```
public static int LIGHT_1
```


Light main color 1.

### LIGHT_2 {#LIGHT-2}
```
public static int LIGHT_2
```


Light main color 2.

### NONE {#NONE}
```
public static int NONE
```


No color.

### TEXT_1 {#TEXT-1}
```
public static int TEXT_1
```


Text color 1.

### TEXT_2 {#TEXT-2}
```
public static int TEXT_2
```


Text color 2.

### length {#length}
```
public static int length
```


### fromName(String themeColorName) {#fromName-java.lang.String}
```
public static int fromName(String themeColorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| themeColorName | java.lang.String |  |

**Returns:**
int
### getName(int themeColor) {#getName-int}
```
public static String getName(int themeColor)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| themeColor | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int themeColor) {#toString-int}
```
public static String toString(int themeColor)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| themeColor | int |  |

**Returns:**
java.lang.String
