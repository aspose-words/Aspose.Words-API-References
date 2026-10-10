---
title: "TextOrientation"
linktitle: "TextOrientation"
second_title: "Aspose.Words für Java"
description: "Gibt die Ausrichtung des Textes auf einer Seite in einer Tabellenzelle oder einem Textrahmen in Java an."
type: docs
weight: 675
url: /de/java/com.aspose.words/textorientation/
---

**Inheritance:**
java.lang.Object
```
public class TextOrientation
```

Gibt die Ausrichtung des Textes auf einer Seite, in einer Tabellenzelle oder einem Textrahmen an.

 **Examples:** 

Zeigt, wie man eine formatierte 2x2-Tabelle erstellt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Der Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Der Text wird horizontal angeordnet (lr-tb). |
| [HORIZONTAL_ROTATED_FAR_EAST](#HORIZONTAL-ROTATED-FAR-EAST) | Der Text wird horizontal angeordnet, aber ostasiatische Zeichen werden um 90 Grad nach links gedreht (lr-tb-v). |
| [UPWARD](#UPWARD) | Der Text wird um 90 Grad nach links gedreht, sodass er von unten nach oben erscheint (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Ostasiatische Zeichen erscheinen vertikal, anderer Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Ostasiatische Zeichen erscheinen vertikal, anderer Text wird um 90 Grad nach rechts gedreht, sodass er vertikal von oben nach unten erscheint und dann horizontal von links nach rechts (tb-lr-v). |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String textOrientationName)](#fromName-java.lang.String) |  |
| [getName(int textOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Der Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Der Text wird horizontal angeordnet (lr-tb).

### HORIZONTAL_ROTATED_FAR_EAST {#HORIZONTAL-ROTATED-FAR-EAST}
```
public static int HORIZONTAL_ROTATED_FAR_EAST
```


Der Text wird horizontal angeordnet, aber ostasiatische Zeichen werden um 90 Grad nach links gedreht (lr-tb-v).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Der Text wird um 90 Grad nach links gedreht, sodass er von unten nach oben erscheint (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Ostasiatische Zeichen erscheinen vertikal, anderer Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Ostasiatische Zeichen erscheinen vertikal, anderer Text wird um 90 Grad nach rechts gedreht, sodass er vertikal von oben nach unten erscheint und dann horizontal von links nach rechts (tb-lr-v).

### length {#length}
```
public static int length
```


### fromName(String textOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String textOrientationName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int textOrientation) {#getName-int}
```
public static String getName(int textOrientation)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textOrientation) {#toString-int}
```
public static String toString(int textOrientation)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
