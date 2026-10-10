---
title: "TableAlignment"
linktitle: "TableAlignment"
second_title: "Aspose.Words für Java"
description: "Gibt die Ausrichtung für eine Inline-Tabelle in Java an."
type: docs
weight: 657
url: /de/java/com.aspose.words/tablealignment/
---

**Inheritance:**
java.lang.Object
```
public class TableAlignment
```

Gibt die Ausrichtung für eine Inline‑Tabelle an.

 **Examples:** 

Zeigt, wie man einer Tabelle einen Umrandungsrahmen hinzufügt.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CENTER](#CENTER) | Die Tabelle ist zentriert. |
| [LEFT](#LEFT) | Die Tabelle ist linksbündig ausgerichtet. |
| [RIGHT](#RIGHT) | Die Tabelle ist rechtsbündig ausgerichtet. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String tableAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Die Tabelle ist zentriert.

### LEFT {#LEFT}
```
public static int LEFT
```


Die Tabelle ist linksbündig ausgerichtet.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Die Tabelle ist rechtsbündig ausgerichtet.

### length {#length}
```
public static int length
```


### fromName(String tableAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableAlignment) {#getName-int}
```
public static String getName(int tableAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableAlignment) {#toString-int}
```
public static String toString(int tableAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
