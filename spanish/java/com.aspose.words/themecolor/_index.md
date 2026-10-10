---
title: "ThemeColor"
linktitle: "ThemeColor"
second_title: "Aspose.Words para Java"
description: "Especifica los colores del tema para los temas de documentos en Java."
type: docs
weight: 683
url: /es/java/com.aspose.words/themecolor/
---

**Inheritance:**
java.lang.Object
```
public class ThemeColor
```

Especifica los colores del tema para los temas del documento.

Para obtener más información, visite el artículo de documentación [ Working with Styles and Themes ][Working with Styles and Themes].

 **Remarks:** 

El color de tema especificado es una referencia a uno de los colores de tema predefinidos, ubicado en la parte Theme del documento, lo que permite que la información de color se establezca de forma centralizada en el documento.

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

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

Muestra cómo crear y usar estilos temáticos.

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


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## Campos

| Campo | Descripción |
| --- | --- |
| [ACCENT_1](#ACCENT-1) | Color de acento 1. |
| [ACCENT_2](#ACCENT-2) | Color de acento 2. |
| [ACCENT_3](#ACCENT-3) | Color de acento 3. |
| [ACCENT_4](#ACCENT-4) | Color de acento 4. |
| [ACCENT_5](#ACCENT-5) | Color de acento 5. |
| [ACCENT_6](#ACCENT-6) | Color de acento 6. |
| [BACKGROUND_1](#BACKGROUND-1) | Color de fondo 1. |
| [BACKGROUND_2](#BACKGROUND-2) | Color de fondo 2. |
| [DARK_1](#DARK-1) | Color principal oscuro 1. |
| [DARK_2](#DARK-2) | Color principal oscuro 2. |
| [FOLLOWED_HYPERLINK](#FOLLOWED-HYPERLINK) | Color de hipervínculo visitado. |
| [HYPERLINK](#HYPERLINK) | Color de hipervínculo. |
| [LIGHT_1](#LIGHT-1) | Color principal claro 1. |
| [LIGHT_2](#LIGHT-2) | Color principal claro 2. |
| [NONE](#NONE) | Sin color. |
| [TEXT_1](#TEXT-1) | Color de texto 1. |
| [TEXT_2](#TEXT-2) | Color de texto 2. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String themeColorName)](#fromName-java.lang.String) |  |
| [getName(int themeColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int themeColor)](#toString-int) |  |
### ACCENT_1 {#ACCENT-1}
```
public static int ACCENT_1
```


Color de acento 1.

### ACCENT_2 {#ACCENT-2}
```
public static int ACCENT_2
```


Color de acento 2.

### ACCENT_3 {#ACCENT-3}
```
public static int ACCENT_3
```


Color de acento 3.

### ACCENT_4 {#ACCENT-4}
```
public static int ACCENT_4
```


Color de acento 4.

### ACCENT_5 {#ACCENT-5}
```
public static int ACCENT_5
```


Color de acento 5.

### ACCENT_6 {#ACCENT-6}
```
public static int ACCENT_6
```


Color de acento 6.

### BACKGROUND_1 {#BACKGROUND-1}
```
public static int BACKGROUND_1
```


Color de fondo 1.

### BACKGROUND_2 {#BACKGROUND-2}
```
public static int BACKGROUND_2
```


Color de fondo 2.

### DARK_1 {#DARK-1}
```
public static int DARK_1
```


Color principal oscuro 1.

### DARK_2 {#DARK-2}
```
public static int DARK_2
```


Color principal oscuro 2.

### FOLLOWED_HYPERLINK {#FOLLOWED-HYPERLINK}
```
public static int FOLLOWED_HYPERLINK
```


Color de hipervínculo visitado.

### HYPERLINK {#HYPERLINK}
```
public static int HYPERLINK
```


Color de hipervínculo.

### LIGHT_1 {#LIGHT-1}
```
public static int LIGHT_1
```


Color principal claro 1.

### LIGHT_2 {#LIGHT-2}
```
public static int LIGHT_2
```


Color principal claro 2.

### NONE {#NONE}
```
public static int NONE
```


Sin color.

### TEXT_1 {#TEXT-1}
```
public static int TEXT_1
```


Color de texto 1.

### TEXT_2 {#TEXT-2}
```
public static int TEXT_2
```


Color de texto 2.

### length {#length}
```
public static int length
```


### fromName(String themeColorName) {#fromName-java.lang.String}
```
public static int fromName(String themeColorName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| themeColorName | java.lang.String |  |

**Returns:**
int
### getName(int themeColor) {#getName-int}
```
public static String getName(int themeColor)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| themeColor | int |  |

**Returns:**
java.lang.String
