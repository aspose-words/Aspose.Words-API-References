---
title: "PreferredWidthType"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words für Java"
description: "Gibt die Maßeinheit für die bevorzugte Breite einer Tabelle oder Zelle in Java an."
type: docs
weight: 551
url: /de/java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

Gibt die Maßeinheit für die bevorzugte Breite einer Tabelle oder Zelle an.

 **Examples:** 

Zeigt, wie man den bevorzugten Breitentyp und -wert einer Tabellenzelle überprüft.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Die bevorzugte Breite ist nicht angegeben. |
| [PERCENT](#PERCENT) | Messen Sie die aktuelle Elementbreite mithilfe eines angegebenen Prozentsatzes. |
| [POINTS](#POINTS) | Messen Sie die aktuelle Elementbreite mithilfe einer angegebenen Punktzahl (1/72 Zoll). |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Die bevorzugte Breite ist nicht angegeben. Die tatsächliche Breite der Tabelle oder Zelle wird entweder über die explizite Breite festgelegt oder beim Anzeigen der Tabelle automatisch vom Tabellenlayout‑Algorithmus bestimmt, abhängig von der Auto‑Fit‑Einstellung der Tabelle.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Messen Sie die aktuelle Elementbreite mithilfe eines angegebenen Prozentsatzes.

### POINTS {#POINTS}
```
public static int POINTS
```


Messen Sie die aktuelle Elementbreite mithilfe einer angegebenen Punktzahl (1/72 Zoll).

### length {#length}
```
public static int length
```


### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
