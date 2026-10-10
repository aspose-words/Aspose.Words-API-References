---
title: "ThemeFont"
linktitle: "ThemeFont"
second_title: "Aspose.Words per Java"
description: "Specifica i tipi di nomi di caratteri tematici per i temi dei documenti in Java."
type: docs
weight: 685
url: /it/java/com.aspose.words/themefont/
---

**Inheritance:**
java.lang.Object
```
public class ThemeFont
```

Specifica i tipi di nomi di caratteri del tema per i temi del documento.

 **Remarks:** 

Specifica un tipo di font tematico che può essere referenziato come font tematico nelle proprietà dell'oggetto padre. Questo font tematico è un riferimento a uno dei font tematici predefiniti, situato nella parte Theme del documento, il che consente di impostare le informazioni sul font in modo centralizzato nel documento.

 **Examples:** 

Mostra come lavorare con i font tematici e i colori.

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

Mostra come creare e utilizzare lo stile tematico.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [MAJOR](#MAJOR) | Font tematico principale. |
| [MINOR](#MINOR) | Font tematico secondario. |
| [NONE](#NONE) | Nessun font tematico. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String themeFontName)](#fromName-java.lang.String) |  |
| [getName(int themeFont)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int themeFont)](#toString-int) |  |
### MAJOR {#MAJOR}
```
public static int MAJOR
```


Font tematico principale.

### MINOR {#MINOR}
```
public static int MINOR
```


Font tematico secondario.

### NONE {#NONE}
```
public static int NONE
```


Nessun font tematico.

### length {#length}
```
public static int length
```


### fromName(String themeFontName) {#fromName-java.lang.String}
```
public static int fromName(String themeFontName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| themeFontName | java.lang.String |  |

**Returns:**
int
### getName(int themeFont) {#getName-int}
```
public static String getName(int themeFont)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| themeFont | int |  |

**Returns:**
java.lang.String
