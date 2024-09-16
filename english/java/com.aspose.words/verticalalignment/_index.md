---
title: VerticalAlignment
linktitle: VerticalAlignment
second_title: Aspose.Words for Java
description: Specifies vertical alignment of a floating shape text frame or a floating table in Java.
type: docs
weight: 662
url: /java/com.aspose.words/verticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class VerticalAlignment
```

Specifies vertical alignment of a floating shape, text frame or a floating table.

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
| [BOTTOM](#BOTTOM) | Specifies that the object shall be at the bottom of the vertical alignment base. |
| [CENTER](#CENTER) | Specifies that the object shall be centered with respect to the vertical alignment base. |
| [DEFAULT](#DEFAULT) | Same as [NONE](../../com.aspose.words/verticalalignment/\#NONE). |
| [INLINE](#INLINE) | Not documented. |
| [INSIDE](#INSIDE) | Specifies that the object shall be inside of the horizontal alignment base. |
| [NONE](#NONE) | The object is explicitly positioned, usually using its **Top** property. |
| [OUTSIDE](#OUTSIDE) | Specifies that the object shall be outside of the vertical alignment base. |
| [TOP](#TOP) | Specifies that the object shall be at the top of the vertical alignment base. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String verticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int verticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int verticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Specifies that the object shall be at the bottom of the vertical alignment base.

### CENTER {#CENTER}
```
public static int CENTER
```


Specifies that the object shall be centered with respect to the vertical alignment base.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Same as [NONE](../../com.aspose.words/verticalalignment/\#NONE).

### INLINE {#INLINE}
```
public static int INLINE
```


Not documented. Seems to be a possible value for floating paragraphs and tables.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Specifies that the object shall be inside of the horizontal alignment base.

### NONE {#NONE}
```
public static int NONE
```


The object is explicitly positioned, usually using its **Top** property.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Specifies that the object shall be outside of the vertical alignment base.

### TOP {#TOP}
```
public static int TOP
```


Specifies that the object shall be at the top of the vertical alignment base.

### length {#length}
```
public static int length
```


### fromName(String verticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String verticalAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| verticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int verticalAlignment) {#getName-int}
```
public static String getName(int verticalAlignment)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
