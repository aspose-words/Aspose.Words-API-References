---
title: "WrapType"
linktitle: "WrapType"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Text in Java um eine Form oder ein Bild gewickelt wird."
type: docs
weight: 737
url: /de/java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

Gibt an, wie Text um eine Form oder ein Bild herumfließt.

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
| [INLINE](#INLINE) | Die Form bleibt in derselben Ebene wie der Text und wird als Zeichen behandelt. |
| [NONE](#NONE) | Kein Textumbruch um die Form. |
| [SQUARE](#SQUARE) | Umwickelt den Text um alle Seiten des quadratischen Begrenzungsrahmens der Form. |
| [THROUGH](#THROUGH) | Wie Tight, aber umwickelt auch offene Teile der Form. |
| [TIGHT](#TIGHT) | Umwickelt die Kanten der Form eng, anstatt um den Begrenzungsrahmen zu wickeln. |
| [TOP_BOTTOM](#TOP-BOTTOM) | Der Text stoppt oben an der Form und beginnt in der Zeile unterhalb der Form neu. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapType)](#toString-int) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


Die Form bleibt in derselben Ebene wie der Text und wird als Zeichen behandelt.

### NONE {#NONE}
```
public static int NONE
```


Kein Textumbruch um die Form. Die Form wird hinter oder vor dem Text platziert.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Umwickelt den Text um alle Seiten des quadratischen Begrenzungsrahmens der Form.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


Wie Tight, aber umwickelt auch offene Teile der Form.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Umwickelt die Kanten der Form eng, anstatt um den Begrenzungsrahmen zu wickeln.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


Der Text stoppt oben an der Form und beginnt in der Zeile unterhalb der Form neu.

### length {#length}
```
public static int length
```


### fromName(String wrapTypeName) {#fromName-java.lang.String}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getName(int wrapType) {#getName-int}
```
public static String getName(int wrapType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int wrapType) {#toString-int}
```
public static String toString(int wrapType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
