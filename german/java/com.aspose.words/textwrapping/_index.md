---
title: "TextWrapping"
linktitle: "TextWrapping"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Text in Java um die Tabelle herumgebrochen wird."
type: docs
weight: 679
url: /de/java/com.aspose.words/textwrapping/
---

**Inheritance:**
java.lang.Object
```
public class TextWrapping
```

Gibt an, wie Text um die Tabelle herumfließt.

 **Examples:** 

Zeigt, wie man mit dem Zeilenumbruch von Tabellen arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 builder.getFont().setSize(16.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
 // and push it down into the paragraph below by setting the position.
 table.setTextWrapping(TextWrapping.AROUND);
 table.setAbsoluteHorizontalDistance(100.0);
 table.setAbsoluteVerticalDistance(20.0);

 doc.save(getArtifactsDir() + "Table.WrapText.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AROUND](#AROUND) | Text wird um die Tabelle herumgebrochen und nutzt den verfügbaren Seitenraum. |
| [DEFAULT](#DEFAULT) | Standardwert. |
| [NONE](#NONE) | Text und Tabelle werden in der Reihenfolge ihres Auftretens im Dokument angezeigt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String textWrappingName)](#fromName-java.lang.String) |  |
| [getName(int textWrapping)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textWrapping)](#toString-int) |  |
### AROUND {#AROUND}
```
public static int AROUND
```


Text wird um die Tabelle herumgebrochen und nutzt den verfügbaren Seitenraum.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert.

### NONE {#NONE}
```
public static int NONE
```


Text und Tabelle werden in der Reihenfolge ihres Auftretens im Dokument angezeigt.

### length {#length}
```
public static int length
```


### fromName(String textWrappingName) {#fromName-java.lang.String}
```
public static int fromName(String textWrappingName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textWrappingName | java.lang.String |  |

**Returns:**
int
### getName(int textWrapping) {#getName-int}
```
public static String getName(int textWrapping)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textWrapping) {#toString-int}
```
public static String toString(int textWrapping)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
