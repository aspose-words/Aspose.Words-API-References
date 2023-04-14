---
title: HtmlOfficeMathOutputMode
linktitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words for Java API Reference
description: Specifies how Aspose.Words exports OfficeMath to HTML MHTML and EPUB in Java.
type: docs
weight: 333
url: /java/com.aspose.words/htmlofficemathoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlOfficeMathOutputMode
```

Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB.

 **Examples:** 

Shows how to specify how to export Microsoft OfficeMath objects to HTML.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles OfficeMath objects.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
 // will render each OfficeMath object into an image.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
 // will convert each OfficeMath object into MathML.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
 // will represent each OfficeMath formula using plain HTML text.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setOfficeMathOutputMode(htmlOfficeMathOutputMode);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
 
```
## Fields

| Field | Description |
| --- | --- |
| [IMAGE](#IMAGE) | OfficeMath is converted to HTML as image specified by ![Image 1][] tag.


[Image 1]:  |
| [MATH_ML](#MATH-ML) | OfficeMath is converted to HTML using MathML. |
| [TEXT](#TEXT) | OfficeMath is converted to HTML as sequence of runs specified by  tags. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String htmlOfficeMathOutputModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int htmlOfficeMathOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int htmlOfficeMathOutputMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


OfficeMath is converted to HTML as image specified by ![Image 1][] tag.


[Image 1]: 

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


OfficeMath is converted to HTML using MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


OfficeMath is converted to HTML as sequence of runs specified by  tags.

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
### fromName(String htmlOfficeMathOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlOfficeMathOutputModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int htmlOfficeMathOutputMode) {#getName-int}
```
public static String getName(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

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
### toString(int htmlOfficeMathOutputMode) {#toString-int}
```
public static String toString(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

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

