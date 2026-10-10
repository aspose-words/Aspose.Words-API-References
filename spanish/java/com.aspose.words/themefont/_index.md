---
title: "ThemeFont"
linktitle: "ThemeFont"
second_title: "Aspose.Words para Java"
description: "Especifica los tipos de nombres de fuentes de tema para los temas de documentos en Java."
type: docs
weight: 685
url: /es/java/com.aspose.words/themefont/
---

**Inheritance:**
java.lang.Object
```
public class ThemeFont
```

Especifica los tipos de nombres de fuentes del tema para los temas del documento.

 **Remarks:** 

Especifica un tipo de fuente de tema que puede ser referenciado como una fuente de tema dentro de las propiedades del objeto padre. Esta fuente de tema es una referencia a una de las fuentes de tema predefinidas, ubicadas en la parte Theme del documento, lo que permite que la información de la fuente se establezca de forma centralizada en el documento.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [MAJOR](#MAJOR) | Fuente de tema principal. |
| [MINOR](#MINOR) | Fuente de tema secundaria. |
| [NONE](#NONE) | Sin fuente de tema. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String themeFontName)](#fromName-java.lang.String) |  |
| [getName(int themeFont)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int themeFont)](#toString-int) |  |
### MAJOR {#MAJOR}
```
public static int MAJOR
```


Fuente de tema principal.

### MINOR {#MINOR}
```
public static int MINOR
```


Fuente de tema secundaria.

### NONE {#NONE}
```
public static int NONE
```


Sin fuente de tema.

### length {#length}
```
public static int length
```


### fromName(String themeFontName) {#fromName-java.lang.String}
```
public static int fromName(String themeFontName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| themeFontName | java.lang.String |  |

**Returns:**
int
### getName(int themeFont) {#getName-int}
```
public static String getName(int themeFont)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| themeFont | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int themeFont) {#toString-int}
```
public static String toString(int themeFont)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| themeFont | int |  |

**Returns:**
java.lang.String
