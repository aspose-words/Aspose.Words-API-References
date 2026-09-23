---
title: "RelativeVerticalPosition"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words für Java"
description: "Gibt an, worauf sich die vertikale Position einer Form oder eines Textfelds in Java bezieht."
type: docs
weight: 563
url: /de/java/com.aspose.words/relativeverticalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalPosition
```

Gibt an, worauf sich die vertikale Position einer Form oder eines Textfelds bezieht.

 **Examples:** 

Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Gibt an, dass die vertikale Positionierung relativ zum unteren Rand der aktuellen Seite sein soll. |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Gibt an, dass die vertikale Positionierung relativ zum inneren Rand der aktuellen Seite sein soll. |
| [LINE](#LINE) | Undokumentiert. |
| [MARGIN](#MARGIN) | Gibt an, dass die vertikale Positionierung relativ zu den Seitenrändern sein soll. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Gibt an, dass die vertikale Positionierung relativ zum äußeren Rand der aktuellen Seite sein soll. |
| [PAGE](#PAGE) | Das Objekt ist relativ zur oberen Kante der Seite positioniert. |
| [PARAGRAPH](#PARAGRAPH) | Das Objekt ist relativ zum oberen Rand des Absatzes positioniert, der den Anker enthält. |
| [TABLE_DEFAULT](#TABLE-DEFAULT) | Standardwert ist [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN). |
| [TEXT_FRAME_DEFAULT](#TEXT-FRAME-DEFAULT) | Standardwert ist [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH). |
| [TOP_MARGIN](#TOP-MARGIN) | Gibt an, dass die vertikale Positionierung relativ zum oberen Rand der aktuellen Seite sein soll. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String relativeVerticalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalPosition)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Gibt an, dass die vertikale Positionierung relativ zum unteren Rand der aktuellen Seite sein soll.

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Gibt an, dass die vertikale Positionierung relativ zum inneren Rand der aktuellen Seite sein soll.

### LINE {#LINE}
```
public static int LINE
```


Undokumentiert.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Gibt an, dass die vertikale Positionierung relativ zu den Seitenrändern sein soll.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Gibt an, dass die vertikale Positionierung relativ zum äußeren Rand der aktuellen Seite sein soll.

### PAGE {#PAGE}
```
public static int PAGE
```


Das Objekt ist relativ zur oberen Kante der Seite positioniert.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Das Objekt ist relativ zum oberen Rand des Absatzes positioniert, der den Anker enthält.

### TABLE_DEFAULT {#TABLE-DEFAULT}
```
public static int TABLE_DEFAULT
```


Standardwert ist [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

### TEXT_FRAME_DEFAULT {#TEXT-FRAME-DEFAULT}
```
public static int TEXT_FRAME_DEFAULT
```


Standardwert ist [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Gibt an, dass die vertikale Positionierung relativ zum oberen Rand der aktuellen Seite sein soll.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalPositionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeVerticalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalPosition) {#getName-int}
```
public static String getName(int relativeVerticalPosition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalPosition) {#toString-int}
```
public static String toString(int relativeVerticalPosition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
