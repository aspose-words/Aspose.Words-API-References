---
title: HtmlFixedPageHorizontalAlignment
linktitle: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words for Java
description: Specifies the horizontal alignment for pages in output HTML document in Java.
type: docs
weight: 337
url: /java/com.aspose.words/htmlfixedpagehorizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HtmlFixedPageHorizontalAlignment
```

Specifies the horizontal alignment for pages in output HTML document.

 **Examples:** 

Shows how to set the horizontal alignment of pages when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setPageHorizontalAlignment(pageHorizontalAlignment);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css"), StandardCharsets.UTF_8);

 switch (pageHorizontalAlignment)
 {
     case HtmlFixedPageHorizontalAlignment.CENTER:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.LEFT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.RIGHT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [CENTER](#CENTER) | Center pages. |
| [LEFT](#LEFT) | Align pages to the left. |
| [RIGHT](#RIGHT) | Align pages to the right. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String htmlFixedPageHorizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int htmlFixedPageHorizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int htmlFixedPageHorizontalAlignment)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Center pages. This is the default value.

### LEFT {#LEFT}
```
public static int LEFT
```


Align pages to the left.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Align pages to the right.

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
### fromName(String htmlFixedPageHorizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String htmlFixedPageHorizontalAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int htmlFixedPageHorizontalAlignment) {#getName-int}
```
public static String getName(int htmlFixedPageHorizontalAlignment)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignment | int |  |

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
### toString(int htmlFixedPageHorizontalAlignment) {#toString-int}
```
public static String toString(int htmlFixedPageHorizontalAlignment)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignment | int |  |

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

