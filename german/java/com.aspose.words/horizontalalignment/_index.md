---
title: "HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words für Java"
description: "Gibt die horizontale Ausrichtung eines schwebenden Form-Textframes oder einer schwebenden Tabelle in Java an."
type: docs
weight: 374
url: /de/java/com.aspose.words/horizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalAlignment
```

Gibt die horizontale Ausrichtung einer schwebenden Form, eines Textfelds oder einer schwebenden Tabelle an.

 **Examples:** 

Zeigt, wie man ein schwebendes Bild in die Mitte einer Seite einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CENTER](#CENTER) | Gibt an, dass das Objekt relativ zur Basis der horizontalen Ausrichtung zentriert sein soll. |
| [DEFAULT](#DEFAULT) | Entspricht [NONE](../../com.aspose.words/horizontalalignment/\#NONE). |
| [INSIDE](#INSIDE) | Gibt an, dass das Objekt innerhalb der horizontalen Ausrichtungsbasis liegen soll. |
| [LEFT](#LEFT) | Gibt an, dass das Objekt linksbündig zur Basis der horizontalen Ausrichtung ausgerichtet sein soll. |
| [NONE](#NONE) | Das Objekt ist explizit positioniert, normalerweise über seine **Left**-Eigenschaft. |
| [OUTSIDE](#OUTSIDE) | Gibt an, dass das Objekt außerhalb der Basis der horizontalen Ausrichtung liegen soll. |
| [RIGHT](#RIGHT) | Gibt an, dass das Objekt rechtsbündig zur Basis der horizontalen Ausrichtung ausgerichtet sein soll. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String horizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Gibt an, dass das Objekt relativ zur Basis der horizontalen Ausrichtung zentriert sein soll.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Entspricht [NONE](../../com.aspose.words/horizontalalignment/\#NONE).

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Gibt an, dass das Objekt innerhalb der horizontalen Ausrichtungsbasis liegen soll.

### LEFT {#LEFT}
```
public static int LEFT
```


Gibt an, dass das Objekt linksbündig zur Basis der horizontalen Ausrichtung ausgerichtet sein soll.

### NONE {#NONE}
```
public static int NONE
```


Das Objekt ist explizit positioniert, normalerweise über seine **Left**-Eigenschaft.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Gibt an, dass das Objekt außerhalb der Basis der horizontalen Ausrichtung liegen soll.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Gibt an, dass das Objekt rechtsbündig zur Basis der horizontalen Ausrichtung ausgerichtet sein soll.

### length {#length}
```
public static int length
```


### fromName(String horizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| horizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalAlignment) {#getName-int}
```
public static String getName(int horizontalAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int horizontalAlignment) {#toString-int}
```
public static String toString(int horizontalAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
