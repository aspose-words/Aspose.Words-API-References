---
title: PageVerticalAlignment
linktitle: PageVerticalAlignment
second_title: Aspose.Words for Java
description: Specifies vertical justification of text on each page in Java.
type: docs
weight: 458
url: /java/com.aspose.words/pageverticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class PageVerticalAlignment
```

Specifies vertical justification of text on each page.

 **Examples:** 

Shows how to apply and revert page setup settings to sections in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Text is aligned at the bottom of the page. |
| [CENTER](#CENTER) | Text is aligned in the middle of the page. |
| [JUSTIFY](#JUSTIFY) | Text is spread to fill the page. |
| [TOP](#TOP) | Text is aligned at the top of the page. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String pageVerticalAlignmentName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int pageVerticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int pageVerticalAlignment)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Text is aligned at the bottom of the page.

### CENTER {#CENTER}
```
public static int CENTER
```


Text is aligned in the middle of the page.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Text is spread to fill the page.

### TOP {#TOP}
```
public static int TOP
```


Text is aligned at the top of the page.

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
### fromName(String pageVerticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String pageVerticalAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageVerticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int pageVerticalAlignment) {#getName-int}
```
public static String getName(int pageVerticalAlignment)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageVerticalAlignment | int |  |

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
### toString(int pageVerticalAlignment) {#toString-int}
```
public static String toString(int pageVerticalAlignment)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageVerticalAlignment | int |  |

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

