---
title: PageBorderDistanceFrom
linktitle: PageBorderDistanceFrom
second_title: Aspose.Words for Java API Reference
description: Specifies the positioning of the page border relative to the page margin in Java.
type: docs
weight: 440
url: /java/com.aspose.words/pageborderdistancefrom/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderDistanceFrom
```

Specifies the positioning of the page border relative to the page margin.

 **Examples:** 

Shows how to create a wide blue band border at the top of the first page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [PAGE_EDGE](#PAGE-EDGE) | Border position is measured from the page edge. |
| [TEXT](#TEXT) | Border position is measured from the page margin. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String pageBorderDistanceFromName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int pageBorderDistanceFrom)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int pageBorderDistanceFrom)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### PAGE_EDGE {#PAGE-EDGE}
```
public static int PAGE_EDGE
```


Border position is measured from the page edge.

### TEXT {#TEXT}
```
public static int TEXT
```


Border position is measured from the page margin.

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
### fromName(String pageBorderDistanceFromName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderDistanceFromName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageBorderDistanceFromName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int pageBorderDistanceFrom) {#getName-int}
```
public static String getName(int pageBorderDistanceFrom)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

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
### toString(int pageBorderDistanceFrom) {#toString-int}
```
public static String toString(int pageBorderDistanceFrom)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

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

