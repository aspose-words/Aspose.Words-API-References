---
title: WrapType
linktitle: WrapType
second_title: Aspose.Words for Java
description: Specifies how text is wrapped around a shape or picture in Java.
type: docs
weight: 725
url: /java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

Specifies how text is wrapped around a shape or picture.

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

Shows how to insert an image, and use it as a watermark.

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
## Fields

| Field | Description |
| --- | --- |
| [INLINE](#INLINE) | The shape remains on the same layer as text and treated as a character. |
| [NONE](#NONE) | No text wrapping around the shape. |
| [SQUARE](#SQUARE) | Wraps text around all sides of the square bounding box of the shape. |
| [THROUGH](#THROUGH) | Same as Tight, but wraps inside any parts of the shape that are open. |
| [TIGHT](#TIGHT) | Wraps tightly around the edges of the shape, instead of wrapping around the bounding box. |
| [TOP_BOTTOM](#TOP-BOTTOM) | The text stops at the top of the shape and restarts on the line below the shape. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapType)](#toString-int) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


The shape remains on the same layer as text and treated as a character.

### NONE {#NONE}
```
public static int NONE
```


No text wrapping around the shape. The shape is placed behind or in front of text.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Wraps text around all sides of the square bounding box of the shape.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


Same as Tight, but wraps inside any parts of the shape that are open.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Wraps tightly around the edges of the shape, instead of wrapping around the bounding box.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


The text stops at the top of the shape and restarts on the line below the shape.

### length {#length}
```
public static int length
```


### fromName(String wrapTypeName) {#fromName-java.lang.String}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getName(int wrapType) {#getName-int}
```
public static String getName(int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
