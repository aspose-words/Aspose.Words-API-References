---
title: LayoutEntityType
linktitle: LayoutEntityType
second_title: Aspose.Words for Java API Reference
description: Types of the layout entities in Java.
type: docs
weight: 362
url: /java/com.aspose.words/layoutentitytype/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEntityType
```

Types of the layout entities.
## Fields

| Field | Description |
| --- | --- |
| [CELL](#CELL) | Represents a table cell. |
| [COLUMN](#COLUMN) | Represents a column of text on a page. |
| [COMMENT](#COMMENT) | Represents placeholder for comment content. |
| [ENDNOTE](#ENDNOTE) | Represents placeholder for endnote content. |
| [FOOTNOTE](#FOOTNOTE) | Represents placeholder for footnote content. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Represents placeholder for header/footer content on a page. |
| [LINE](#LINE) | Represents line of characters of text and inline objects. |
| [NONE](#NONE) | Default value. |
| [NOTE](#NOTE) | Represents placeholder for note content. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Represents footnote/endnote separator. |
| [PAGE](#PAGE) | Represents page of a document. |
| [ROW](#ROW) | Represents a table row. |
| [SPAN](#SPAN) | Represents one or more characters in a line. |
| [TEXT_BOX](#TEXT-BOX) | Represents text area inside of a shape. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String layoutEntityTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set layoutEntityTypeNames)](#fromNames-java.util.Set) |  |
| [getClass()](#getClass) |  |
| [getName(int layoutEntityType)](#getName-int) |  |
| [getNames(int layoutEntityType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int layoutEntityType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CELL {#CELL}
```
public static int CELL
```


Represents a table cell. Cell may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Represents a column of text on a page. Column may have the same child entities as [CELL](../../com.aspose.words/layoutentitytype/\#CELL), plus [FOOTNOTE](../../com.aspose.words/layoutentitytype/\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype/\#ENDNOTE) and [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype/\#NOTE-SEPARATOR) entities.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Represents placeholder for comment content. Comment may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


Represents placeholder for endnote content. Endnote may have [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) child entities.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Represents placeholder for footnote content. Footnote may have [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) child entities.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Represents placeholder for header/footer content on a page. HeaderFooter may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### LINE {#LINE}
```
public static int LINE
```


Represents line of characters of text and inline objects. Line may have [SPAN](../../com.aspose.words/layoutentitytype/\#SPAN) child entities.

### NONE {#NONE}
```
public static int NONE
```


Default value.

### NOTE {#NOTE}
```
public static int NOTE
```


Represents placeholder for note content. Note may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


Represents footnote/endnote separator. NoteSeparator may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### PAGE {#PAGE}
```
public static int PAGE
```


Represents page of a document. Page may have [COLUMN](../../com.aspose.words/layoutentitytype/\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype/\#HEADER-FOOTER) and [COMMENT](../../com.aspose.words/layoutentitytype/\#COMMENT) child entities.

### ROW {#ROW}
```
public static int ROW
```


Represents a table row. Row may have [CELL](../../com.aspose.words/layoutentitytype/\#CELL) as child entities.

### SPAN {#SPAN}
```
public static int SPAN
```


Represents one or more characters in a line. This include special characters like field start/end markers, bookmarks and comments. Span may not have child entities.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Represents text area inside of a shape. Textbox may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

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
### fromName(String layoutEntityTypeName) {#fromName-java.lang.String}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int layoutEntityType) {#getName-int}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.util.Set
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
### toString(int layoutEntityType) {#toString-int}
```
public static String toString(int layoutEntityType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

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

