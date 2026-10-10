---
title: "TableStyleOptions"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Tabellenstil in Java auf eine Tabelle angewendet wird."
type: docs
weight: 661
url: /de/java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

Gibt an, wie ein Tabellenstil auf eine Tabelle angewendet wird.

 **Examples:** 

Zeigt, wie man eine neue Tabelle erstellt, während man einen Stil anwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [COLUMN_BANDS](#COLUMN-BANDS) | Spaltenbanding bedingte Formatierung anwenden. |
| [DEFAULT](#DEFAULT) | Dies sind die Standardwerte von Microsoft Word. |
| [DEFAULT_2003](#DEFAULT-2003) | Zeilen- und Spaltenbanding wird angewendet. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Bedingte Formatierung für die erste Spalte anwenden. |
| [FIRST_ROW](#FIRST-ROW) | Bedingte Formatierung für die erste Zeile anwenden. |
| [LAST_COLUMN](#LAST-COLUMN) | Bedingte Formatierung für die letzte Spalte anwenden. |
| [LAST_ROW](#LAST-ROW) | Bedingte Formatierung für die letzte Zeile anwenden. |
| [NONE](#NONE) | Keine Tabellenstil-Formatierung wird angewendet. |
| [ROW_BANDS](#ROW-BANDS) | Zeilenbanding bedingte Formatierung anwenden. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String tableStyleOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set tableStyleOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int tableStyleOptions)](#getName-int) |  |
| [getNames(int tableStyleOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableStyleOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### COLUMN_BANDS {#COLUMN-BANDS}
```
public static int COLUMN_BANDS
```


Spaltenbanding bedingte Formatierung anwenden.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Dies sind die Standardwerte von Microsoft Word.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


Zeilen- und Spaltenbanding wird angewendet. Dies ist die Microsoft Word-Standard für alte Formate wie DOC, WML und RTF.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Bedingte Formatierung für die erste Spalte anwenden.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Bedingte Formatierung für die erste Zeile anwenden.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Bedingte Formatierung für die letzte Spalte anwenden.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Bedingte Formatierung für die letzte Zeile anwenden.

### NONE {#NONE}
```
public static int NONE
```


Keine Tabellenstil-Formatierung wird angewendet.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


Zeilenbanding bedingte Formatierung anwenden.

### length {#length}
```
public static int length
```


### fromName(String tableStyleOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int tableStyleOptions) {#getName-int}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableStyleOptions) {#toString-int}
```
public static String toString(int tableStyleOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
