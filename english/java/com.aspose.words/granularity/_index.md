---
title: Granularity
linktitle: Granularity
second_title: Aspose.Words for Java
description: Specifies the granularity of changes to track when comparing two documents in Java.
type: docs
weight: 324
url: /java/com.aspose.words/granularity/
---

**Inheritance:**
java.lang.Object
```
public class Granularity
```

Specifies the granularity of changes to track when comparing two documents.

 **Examples:** 

Shows to specify a granularity while comparing documents.

```

 Document docA = new Document();
 DocumentBuilder builderA = new DocumentBuilder(docA);
 builderA.writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

 Document docB = new Document();
 DocumentBuilder builderB = new DocumentBuilder(docB);
 builderB.writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

 // Specify whether changes are tracking
 // by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setGranularity(granularity);

 docA.compare(docB, "author", new Date(), compareOptions);

 // The first document's collection of revision groups contains all the differences between documents.
 RevisionGroupCollection groups = docA.getRevisions().getGroups();
 Assert.assertEquals(5, groups.getCount());
 
```
## Fields

| Field | Description |
| --- | --- |
| [CHAR_LEVEL](#CHAR-LEVEL) |  |
| [WORD_LEVEL](#WORD-LEVEL) |  |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String granularityName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int granularity)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int granularity)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CHAR_LEVEL {#CHAR-LEVEL}
```
public static int CHAR_LEVEL
```


### WORD_LEVEL {#WORD-LEVEL}
```
public static int WORD_LEVEL
```


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
### fromName(String granularityName) {#fromName-java.lang.String}
```
public static int fromName(String granularityName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| granularityName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int granularity) {#getName-int}
```
public static String getName(int granularity)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| granularity | int |  |

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
### toString(int granularity) {#toString-int}
```
public static String toString(int granularity)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| granularity | int |  |

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

