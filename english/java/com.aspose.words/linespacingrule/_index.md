---
title: LineSpacingRule
linktitle: LineSpacingRule
second_title: Aspose.Words for Java API Reference
description: Specifies line spacing values for a paragraph in Java.
type: docs
weight: 369
url: /java/com.aspose.words/linespacingrule/
---

**Inheritance:**
java.lang.Object
```
public class LineSpacingRule
```

Specifies line spacing values for a paragraph.
## Fields

| Field | Description |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | The line spacing can be greater than or equal to, but never less than, the value specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property. |
| [EXACTLY](#EXACTLY) | The line spacing never changes from the value specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property, even if a larger font is used within the paragraph. |
| [MULTIPLE](#MULTIPLE) | The line spacing is specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property as the number of lines. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String lineSpacingRuleName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int lineSpacingRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int lineSpacingRule)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


The line spacing can be greater than or equal to, but never less than, the value specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


The line spacing never changes from the value specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property, even if a larger font is used within the paragraph.

### MULTIPLE {#MULTIPLE}
```
public static int MULTIPLE
```


The line spacing is specified in the [ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) property as the number of lines. One line equals 12 points.

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
### fromName(String lineSpacingRuleName) {#fromName-java.lang.String}
```
public static int fromName(String lineSpacingRuleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineSpacingRuleName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int lineSpacingRule) {#getName-int}
```
public static String getName(int lineSpacingRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineSpacingRule | int |  |

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
### toString(int lineSpacingRule) {#toString-int}
```
public static String toString(int lineSpacingRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineSpacingRule | int |  |

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

