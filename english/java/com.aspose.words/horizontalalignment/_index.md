---
title: HorizontalAlignment
linktitle: HorizontalAlignment
second_title: Aspose.Words for Java
description: Specifies horizontal alignment of a floating shape text frame or floating table in Java.
type: docs
weight: 373
url: /java/com.aspose.words/horizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalAlignment
```

Specifies horizontal alignment of a floating shape, text frame or floating table.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

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
## Fields

| Field | Description |
| --- | --- |
| [CENTER](#CENTER) | Specifies that the object shall be centered with respect to the horizontal alignment base. |
| [DEFAULT](#DEFAULT) | Same as [NONE](../../com.aspose.words/horizontalalignment/\#NONE). |
| [INSIDE](#INSIDE) | Specifies that the object shall be inside of the horizontal alignment base. |
| [LEFT](#LEFT) | Specifies that the object shall be left aligned to the horizontal alignment base. |
| [NONE](#NONE) | The object is explicitly positioned, usually using its **Left** property. |
| [OUTSIDE](#OUTSIDE) | Specifies that the object shall be outside of the horizontal alignment base. |
| [RIGHT](#RIGHT) | Specifies that the object shall be right aligned to the horizontal alignment base. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String horizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Specifies that the object shall be centered with respect to the horizontal alignment base.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Same as [NONE](../../com.aspose.words/horizontalalignment/\#NONE).

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Specifies that the object shall be inside of the horizontal alignment base.

### LEFT {#LEFT}
```
public static int LEFT
```


Specifies that the object shall be left aligned to the horizontal alignment base.

### NONE {#NONE}
```
public static int NONE
```


The object is explicitly positioned, usually using its **Left** property.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Specifies that the object shall be outside of the horizontal alignment base.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Specifies that the object shall be right aligned to the horizontal alignment base.

### length {#length}
```
public static int length
```


### fromName(String horizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| horizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalAlignment) {#getName-int}
```
public static String getName(int horizontalAlignment)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
