---
title: LayoutEntityType
second_title: Aspose.Words for Java API Reference
description: Types of the layout entities.
type: docs
weight: 359
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
| [NONE](#NONE) | Default value. |
| [PAGE](#PAGE) | Represents page of a document. |
| [COLUMN](#COLUMN) | Represents a column of text on a page. |
| [ROW](#ROW) | Represents a table row. |
| [CELL](#CELL) | Represents a table cell. |
| [LINE](#LINE) | Represents line of characters of text and inline objects. |
| [SPAN](#SPAN) | Represents one or more characters in a line. |
| [FOOTNOTE](#FOOTNOTE) | Represents placeholder for footnote content. |
| [ENDNOTE](#ENDNOTE) | Represents placeholder for endnote content. |
| [NOTE](#NOTE) | Represents placeholder for note content. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Represents placeholder for header/footer content on a page. |
| [TEXT_BOX](#TEXT-BOX) | Represents text area inside of a shape. |
| [COMMENT](#COMMENT) | Represents placeholder for comment content. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Represents footnote/endnote separator. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int layoutEntityType)](#getName-int-) |  |
| [getNames(int layoutEntityType)](#getNames-int-) |  |
| [toString(int layoutEntityType)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [fromName(String layoutEntityTypeName)](#fromName-java.lang.String-) |  |
| [fromNames(Set layoutEntityTypeNames)](#fromNames-java.util.Set-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


Default value.

### PAGE {#PAGE}
```
public static int PAGE
```


Represents page of a document. Page may have [COLUMN](../../com.aspose.words/layoutentitytype\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype\#HEADER-FOOTER) and [COMMENT](../../com.aspose.words/layoutentitytype\#COMMENT) child entities.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Represents a column of text on a page. Column may have the same child entities as [CELL](../../com.aspose.words/layoutentitytype\#CELL), plus [FOOTNOTE](../../com.aspose.words/layoutentitytype\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype\#ENDNOTE) and [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype\#NOTE-SEPARATOR) entities.

### ROW {#ROW}
```
public static int ROW
```


Represents a table row. Row may have [CELL](../../com.aspose.words/layoutentitytype\#CELL) as child entities.

### CELL {#CELL}
```
public static int CELL
```


Represents a table cell. Cell may have [LINE](../../com.aspose.words/layoutentitytype\#LINE) and [ROW](../../com.aspose.words/layoutentitytype\#ROW) child entities.

### LINE {#LINE}
```
public static int LINE
```


Represents line of characters of text and inline objects. Line may have [SPAN](../../com.aspose.words/layoutentitytype\#SPAN) child entities.

### SPAN {#SPAN}
```
public static int SPAN
```


Represents one or more characters in a line. This include special characters like field start/end markers, bookmarks and comments. Span may not have child entities.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Represents placeholder for footnote content. Footnote may have [NOTE](../../com.aspose.words/layoutentitytype\#NOTE) child entities.

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


Represents placeholder for endnote content. Endnote may have [NOTE](../../com.aspose.words/layoutentitytype\#NOTE) child entities.

### NOTE {#NOTE}
```
public static int NOTE
```


Represents placeholder for note content. Note may have [LINE](../../com.aspose.words/layoutentitytype\#LINE) and [ROW](../../com.aspose.words/layoutentitytype\#ROW) child entities.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Represents placeholder for header/footer content on a page. HeaderFooter may have [LINE](../../com.aspose.words/layoutentitytype\#LINE) and [ROW](../../com.aspose.words/layoutentitytype\#ROW) child entities.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Represents text area inside of a shape. Textbox may have [LINE](../../com.aspose.words/layoutentitytype\#LINE) and [ROW](../../com.aspose.words/layoutentitytype\#ROW) child entities.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Represents placeholder for comment content. Comment may have [LINE](../../com.aspose.words/layoutentitytype\#LINE) and [ROW](../../com.aspose.words/layoutentitytype\#ROW) child entities.

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


Represents footnote/endnote separator. NoteSeparator may have [LINE](../../com.aspose.words/layoutentitytype\#LINE) and [ROW](../../com.aspose.words/layoutentitytype\#ROW) child entities.

### length {#length}
```
public static int length
```


### getName(int layoutEntityType) {#getName-int-}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int-}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.util.Set
### toString(int layoutEntityType) {#toString-int-}
```
public static String toString(int layoutEntityType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
### fromName(String layoutEntityTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
