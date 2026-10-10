---
title: "BorderType"
linktitle: "BorderType"
second_title: "Aspose.Words für Java"
description: "Gibt die Seiten eines Rahmens in Java an."
type: docs
weight: 48
url: /de/java/com.aspose.words/bordertype/
---

**Inheritance:**
java.lang.Object
```
public class BorderType
```

Gibt die Seiten eines Rahmens an.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Zeigt, wie ein Absatz mit einem oberen Rahmen eingefügt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOTTOM](#BOTTOM) | Gibt den unteren Rand eines Absatzes oder einer Tabellenzelle an. |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Gibt den diagonalen Rand in einer Tabellenzelle an. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Gibt den diagonalen Rand in einer Tabellenzelle an. |
| [HORIZONTAL](#HORIZONTAL) | Gibt den horizontalen Rand zwischen Zellen in einer Tabelle oder zwischen zusammengehörigen Absätzen an. |
| [LEFT](#LEFT) | Gibt den linken Rand eines Absatzes oder einer Tabellenzelle an. |
| [NONE](#NONE) | Standardwert. |
| [RIGHT](#RIGHT) | Gibt den rechten Rand eines Absatzes oder einer Tabellenzelle an. |
| [TOP](#TOP) | Gibt den oberen Rand eines Absatzes oder einer Tabellenzelle an. |
| [VERTICAL](#VERTICAL) | Gibt den vertikalen Rand zwischen Zellen in einer Tabelle an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String borderTypeName)](#fromName-java.lang.String) |  |
| [getName(int borderType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int borderType)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Gibt den unteren Rand eines Absatzes oder einer Tabellenzelle an.

### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Gibt den diagonalen Rand in einer Tabellenzelle an.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Gibt den diagonalen Rand in einer Tabellenzelle an.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Gibt den horizontalen Rand zwischen Zellen in einer Tabelle oder zwischen zusammengehörigen Absätzen an.

### LEFT {#LEFT}
```
public static int LEFT
```


Gibt den linken Rand eines Absatzes oder einer Tabellenzelle an.

### NONE {#NONE}
```
public static int NONE
```


Standardwert.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Gibt den rechten Rand eines Absatzes oder einer Tabellenzelle an.

### TOP {#TOP}
```
public static int TOP
```


Gibt den oberen Rand eines Absatzes oder einer Tabellenzelle an.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Gibt den vertikalen Rand zwischen Zellen in einer Tabelle an.

### length {#length}
```
public static int length
```


### fromName(String borderTypeName) {#fromName-java.lang.String}
```
public static int fromName(String borderTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| borderTypeName | java.lang.String |  |

**Returns:**
int
### getName(int borderType) {#getName-int}
```
public static String getName(int borderType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int borderType) {#toString-int}
```
public static String toString(int borderType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
