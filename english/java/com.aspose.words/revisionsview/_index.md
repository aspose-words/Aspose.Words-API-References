---
title: RevisionsView
linktitle: RevisionsView
second_title: Aspose.Words for Java
description: Allows to specify whether to work with the original or revised version of a document in Java.
type: docs
weight: 511
url: /java/com.aspose.words/revisionsview/
---

**Inheritance:**
java.lang.Object
```
public class RevisionsView
```

Allows to specify whether to work with the original or revised version of a document.

 **Examples:** 

Shows how to switch between the revised and the original view of a document.

```

 Document doc = new Document(getMyDir() + "Revisions at list levels.docx");
 doc.updateListLabels();

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();
 Assert.assertEquals("1.", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("", paragraphs.get(2).getListLabel().getLabelString());

 // View the document object as if all the revisions are accepted. Currently supports list labels.
 doc.setRevisionsView(RevisionsView.FINAL);

 Assert.assertEquals("", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("1.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(2).getListLabel().getLabelString());
 
```
## Fields

| Field | Description |
| --- | --- |
| [FINAL](#FINAL) | Specifies revised version of a document. |
| [ORIGINAL](#ORIGINAL) | Specifies original version of a document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String revisionsViewName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int revisionsView)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int revisionsView)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FINAL {#FINAL}
```
public static int FINAL
```


Specifies revised version of a document.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Specifies original version of a document.

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
### fromName(String revisionsViewName) {#fromName-java.lang.String}
```
public static int fromName(String revisionsViewName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionsViewName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int revisionsView) {#getName-int}
```
public static String getName(int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionsView | int |  |

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
### toString(int revisionsView) {#toString-int}
```
public static String toString(int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionsView | int |  |

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

