---
title: "VerticalAlignment"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words für Java"
description: "Gibt die vertikale Ausrichtung eines schwebenden Form-Textrahmens oder einer schwebenden Tabelle in Java an."
type: docs
weight: 713
url: /de/java/com.aspose.words/verticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class VerticalAlignment
```

Gibt die vertikale Ausrichtung einer schwebenden Form, eines Textfelds oder einer schwebenden Tabelle an.

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
| [BOTTOM](#BOTTOM) | Gibt an, dass das Objekt am unteren Rand der vertikalen Ausrichtungsbasis liegen soll. |
| [CENTER](#CENTER) | Gibt an, dass das Objekt bezüglich der vertikalen Ausrichtungsbasis zentriert sein soll. |
| [DEFAULT](#DEFAULT) | Gleich wie [NONE](../../com.aspose.words/verticalalignment/\#NONE). |
| [INLINE](#INLINE) | Nicht dokumentiert. |
| [INSIDE](#INSIDE) | Gibt an, dass das Objekt innerhalb der horizontalen Ausrichtungsbasis liegen soll. |
| [NONE](#NONE) | Das Objekt ist explizit positioniert, normalerweise über seine **Top**-Eigenschaft. |
| [OUTSIDE](#OUTSIDE) | Gibt an, dass das Objekt außerhalb der vertikalen Ausrichtungsbasis liegen soll. |
| [TOP](#TOP) | Gibt an, dass das Objekt am oberen Rand der vertikalen Ausrichtungsbasis liegen soll. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String verticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int verticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int verticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Gibt an, dass das Objekt am unteren Rand der vertikalen Ausrichtungsbasis liegen soll.

### CENTER {#CENTER}
```
public static int CENTER
```


Gibt an, dass das Objekt bezüglich der vertikalen Ausrichtungsbasis zentriert sein soll.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Gleich wie [NONE](../../com.aspose.words/verticalalignment/\#NONE).

### INLINE {#INLINE}
```
public static int INLINE
```


Nicht dokumentiert. Scheint ein möglicher Wert für schwebende Absätze und Tabellen zu sein.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Gibt an, dass das Objekt innerhalb der horizontalen Ausrichtungsbasis liegen soll.

### NONE {#NONE}
```
public static int NONE
```


Das Objekt ist explizit positioniert, normalerweise über seine **Top**-Eigenschaft.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Gibt an, dass das Objekt außerhalb der vertikalen Ausrichtungsbasis liegen soll.

### TOP {#TOP}
```
public static int TOP
```


Gibt an, dass das Objekt am oberen Rand der vertikalen Ausrichtungsbasis liegen soll.

### length {#length}
```
public static int length
```


### fromName(String verticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String verticalAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| verticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int verticalAlignment) {#getName-int}
```
public static String getName(int verticalAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int verticalAlignment) {#toString-int}
```
public static String toString(int verticalAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
