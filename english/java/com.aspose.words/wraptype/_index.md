---
title: WrapType
linktitle: WrapType
second_title: Aspose.Words for Java
description: Specifies how text is wrapped around a shape or picture in Java.
type: docs
weight: 642
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
 BufferedImage image = ImageIO.read(new File(getImageDir() + "Transparent background logo.png"));
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(image);
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int wrapType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

