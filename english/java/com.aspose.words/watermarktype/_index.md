---
title: WatermarkType
linktitle: WatermarkType
second_title: Aspose.Words for Java
description: Specifies the watermark type in Java.
type: docs
weight: 630
url: /java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Specifies the watermark type.

 **Examples:** 

Shows how to create a text watermark.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```
## Fields

| Field | Description |
| --- | --- |
| [IMAGE](#IMAGE) | Indicates that the image will be used as a watermark. |
| [NONE](#NONE) | Indicates watermark is no set. |
| [TEXT](#TEXT) | Indicates that the text will be used as a watermark. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int watermarkType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int watermarkType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


Indicates that the image will be used as a watermark.

Such a watermark corresponds to a shape with image.

### NONE {#NONE}
```
public static int NONE
```


Indicates watermark is no set.

### TEXT {#TEXT}
```
public static int TEXT
```


Indicates that the text will be used as a watermark.

Such a watermark corresponds to a WordArt object.

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
### fromName(String watermarkTypeName) {#fromName-java.lang.String}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int watermarkType) {#getName-int}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkType | int |  |

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
### toString(int watermarkType) {#toString-int}
```
public static String toString(int watermarkType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkType | int |  |

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

