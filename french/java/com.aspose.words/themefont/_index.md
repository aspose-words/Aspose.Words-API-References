---
title: "ThemeFont"
linktitle: "ThemeFont"
second_title: "Aspose.Words pour Java"
description: "Spécifie les types de noms de police de thème pour les thèmes de document en Java."
type: docs
weight: 685
url: /fr/java/com.aspose.words/themefont/
---

**Inheritance:**
java.lang.Object
```
public class ThemeFont
```

Spécifie les types de noms de polices du thème pour les thèmes de document.

 **Remarks:** 

Spécifie un type de police de thème qui peut être référencé comme police de thème dans les propriétés de l'objet parent. Cette police de thème est une référence à l'une des polices de thème prédéfinies, situées dans la partie Thème du document, ce qui permet de définir les informations de police de manière centralisée dans le document.

 **Examples:** 

Montre comment travailler avec les polices de thème et les couleurs.

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

Montre comment créer et utiliser un style thématisé.

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
## Champs

| Champ | Description |
| --- | --- |
| [MAJOR](#MAJOR) | Police de thème principale. |
| [MINOR](#MINOR) | Police de thème secondaire. |
| [NONE](#NONE) | Aucune police de thème. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String themeFontName)](#fromName-java.lang.String) |  |
| [getName(int themeFont)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int themeFont)](#toString-int) |  |
### MAJOR {#MAJOR}
```
public static int MAJOR
```


Police de thème principale.

### MINOR {#MINOR}
```
public static int MINOR
```


Police de thème secondaire.

### NONE {#NONE}
```
public static int NONE
```


Aucune police de thème.

### length {#length}
```
public static int length
```


### fromName(String themeFontName) {#fromName-java.lang.String}
```
public static int fromName(String themeFontName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| themeFontName | java.lang.String |  |

**Returns:**
int
### getName(int themeFont) {#getName-int}
```
public static String getName(int themeFont)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| themeFont | int |  |

**Returns:**
java.lang.String
