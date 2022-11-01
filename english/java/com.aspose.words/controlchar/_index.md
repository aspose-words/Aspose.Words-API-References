---
title: ControlChar
second_title: Aspose.Words for Java API Reference
description: Control characters often encountered in documents.
type: docs
weight: 94
url: /java/com.aspose.words/controlchar/
---

**Inheritance:**
java.lang.Object
```
public class ControlChar
```

Control characters often encountered in documents.

To learn more, visit the **Working With Control Characters** documentation article.

Provides both char and string versions of the same constants. For example: string ControlChar.LineBreak and char ControlChar.LineBreakChar have the same value.
## Fields

| Field | Description |
| --- | --- |
| [CELL](#CELL) | End of a table cell or end of a table row character: "\\x0007" or "\\a". |
| [CELL_CHAR](#CELL-CHAR) | End of a table cell or end of a table row character: (char)7 or "\\a". |
| [COLUMN_BREAK](#COLUMN-BREAK) | End of column character: "\\x000e". |
| [COLUMN_BREAK_CHAR](#COLUMN-BREAK-CHAR) | End of column character: (char)14. |
| [CR](#CR) | Carriage return character: "\\x000d" or "\\r". |
| [CR_LF](#CR-LF) | Carriage return followed by line feed character: "\\x000d\\x000a" or "\\r\\n". |
| [DEFAULT_TEXT_INPUT_CHAR](#DEFAULT-TEXT-INPUT-CHAR) | This is the "o" character used as a default value in text input form fields. |
| [FIELD_END_CHAR](#FIELD-END-CHAR) | End of MS Word field character: (char)21. |
| [FIELD_SEPARATOR_CHAR](#FIELD-SEPARATOR-CHAR) | Field separator character separates field code from field value. |
| [FIELD_START_CHAR](#FIELD-START-CHAR) | Start of MS Word field character: (char)19. |
| [LF](#LF) | Line feed character: "\\x000a" or "\\n". |
| [LINE_BREAK](#LINE-BREAK) | Line break character: "\\x000b" or "\\v". |
| [LINE_BREAK_CHAR](#LINE-BREAK-CHAR) | Line break character: (char)11 or "\\v". |
| [LINE_FEED](#LINE-FEED) | Line feed character: "\\x000a" or "\\n". |
| [LINE_FEED_CHAR](#LINE-FEED-CHAR) | Line feed character: (char)10 or "\\n". |
| [NON_BREAKING_HYPHEN_CHAR](#NON-BREAKING-HYPHEN-CHAR) | Nonbreaking Hyphen in Microsoft Word is (char)30. |
| [NON_BREAKING_SPACE](#NON-BREAKING-SPACE) | Non-breaking space character: "\\x00a0". |
| [NON_BREAKING_SPACE_CHAR](#NON-BREAKING-SPACE-CHAR) | Non-breaking space character: (char)160. |
| [OPTIONAL_HYPHEN_CHAR](#OPTIONAL-HYPHEN-CHAR) | Optional Hyphen in Microsoft Word is (char)31. |
| [PAGE_BREAK](#PAGE-BREAK) | Page break character: "\\x000c" or "\\f". |
| [PAGE_BREAK_CHAR](#PAGE-BREAK-CHAR) | Page break character: (char)12 or "\\f". |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | End of paragraph character: "\\x000d" or "\\r". |
| [PARAGRAPH_BREAK_CHAR](#PARAGRAPH-BREAK-CHAR) | End of paragraph character: (char)13 or "\\r". |
| [SECTION_BREAK](#SECTION-BREAK) | End of section character: "\\x000c" or "\\f". |
| [SECTION_BREAK_CHAR](#SECTION-BREAK-CHAR) | End of section character: (char)12 or "\\f". |
| [SPACE_CHAR](#SPACE-CHAR) | Space character: (char)32. |
| [TAB](#TAB) | Tab character: "\\x0009" or "\\t". |
| [TAB_CHAR](#TAB-CHAR) | Tab character: (char)9 or "\\t". |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CELL {#CELL}
```
public static String CELL
```


End of a table cell or end of a table row character: "\\x0007" or "\\a".

### CELL_CHAR {#CELL-CHAR}
```
public static char CELL_CHAR
```


End of a table cell or end of a table row character: (char)7 or "\\a".

### COLUMN_BREAK {#COLUMN-BREAK}
```
public static String COLUMN_BREAK
```


End of column character: "\\x000e".

### COLUMN_BREAK_CHAR {#COLUMN-BREAK-CHAR}
```
public static char COLUMN_BREAK_CHAR
```


End of column character: (char)14.

### CR {#CR}
```
public static String CR
```


Carriage return character: "\\x000d" or "\\r". Same as [PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK).

### CR_LF {#CR-LF}
```
public static String CR_LF
```


Carriage return followed by line feed character: "\\x000d\\x000a" or "\\r\\n". Not used as such in Microsoft Word documents, but commonly used in text files for paragraph breaks.

### DEFAULT_TEXT_INPUT_CHAR {#DEFAULT-TEXT-INPUT-CHAR}
```
public static char DEFAULT_TEXT_INPUT_CHAR
```


This is the "o" character used as a default value in text input form fields.

### FIELD_END_CHAR {#FIELD-END-CHAR}
```
public static char FIELD_END_CHAR
```


End of MS Word field character: (char)21.

### FIELD_SEPARATOR_CHAR {#FIELD-SEPARATOR-CHAR}
```
public static char FIELD_SEPARATOR_CHAR
```


Field separator character separates field code from field value. Optional in some fields. Value: (char)20.

### FIELD_START_CHAR {#FIELD-START-CHAR}
```
public static char FIELD_START_CHAR
```


Start of MS Word field character: (char)19.

### LF {#LF}
```
public static String LF
```


Line feed character: "\\x000a" or "\\n". Same as [LINE\_FEED](../../com.aspose.words/controlchar\#LINE-FEED).

### LINE_BREAK {#LINE-BREAK}
```
public static String LINE_BREAK
```


Line break character: "\\x000b" or "\\v".

### LINE_BREAK_CHAR {#LINE-BREAK-CHAR}
```
public static char LINE_BREAK_CHAR
```


Line break character: (char)11 or "\\v".

### LINE_FEED {#LINE-FEED}
```
public static String LINE_FEED
```


Line feed character: "\\x000a" or "\\n". Same as [LF](../../com.aspose.words/controlchar\#LF).

### LINE_FEED_CHAR {#LINE-FEED-CHAR}
```
public static char LINE_FEED_CHAR
```


Line feed character: (char)10 or "\\n".

### NON_BREAKING_HYPHEN_CHAR {#NON-BREAKING-HYPHEN-CHAR}
```
public static char NON_BREAKING_HYPHEN_CHAR
```


Nonbreaking Hyphen in Microsoft Word is (char)30.

Nonbreaking Hyphen in Microsoft Word does not correspond to the Unicode character U+2011 non-breaking hyphen but instead represents internal information that tells Microsoft Word to display a hyphen and not to break a line.

Useful info: http://www.cs.tut.fi/~jkorpela/dashes.html\#linebreaks.

### NON_BREAKING_SPACE {#NON-BREAKING-SPACE}
```
public static String NON_BREAKING_SPACE
```


Non-breaking space character: "\\x00a0".

### NON_BREAKING_SPACE_CHAR {#NON-BREAKING-SPACE-CHAR}
```
public static char NON_BREAKING_SPACE_CHAR
```


Non-breaking space character: (char)160.

### OPTIONAL_HYPHEN_CHAR {#OPTIONAL-HYPHEN-CHAR}
```
public static char OPTIONAL_HYPHEN_CHAR
```


Optional Hyphen in Microsoft Word is (char)31.

Optional Hyphen in Microsoft Word does not correspond to the Unicode character U+00AD soft hyphen. Instead, it inserts internal information that tells Word about a possible hyphenation point.

### PAGE_BREAK {#PAGE-BREAK}
```
public static String PAGE_BREAK
```


Page break character: "\\x000c" or "\\f". Note it has the same value as [SECTION\_BREAK](../../com.aspose.words/controlchar\#SECTION-BREAK).

### PAGE_BREAK_CHAR {#PAGE-BREAK-CHAR}
```
public static char PAGE_BREAK_CHAR
```


Page break character: (char)12 or "\\f".

### PARAGRAPH_BREAK {#PARAGRAPH-BREAK}
```
public static String PARAGRAPH_BREAK
```


End of paragraph character: "\\x000d" or "\\r". Same as [CR](../../com.aspose.words/controlchar\#CR)

### PARAGRAPH_BREAK_CHAR {#PARAGRAPH-BREAK-CHAR}
```
public static char PARAGRAPH_BREAK_CHAR
```


End of paragraph character: (char)13 or "\\r".

### SECTION_BREAK {#SECTION-BREAK}
```
public static String SECTION_BREAK
```


End of section character: "\\x000c" or "\\f". Note it has the same value as [PAGE\_BREAK](../../com.aspose.words/controlchar\#PAGE-BREAK).

### SECTION_BREAK_CHAR {#SECTION-BREAK-CHAR}
```
public static char SECTION_BREAK_CHAR
```


End of section character: (char)12 or "\\f".

### SPACE_CHAR {#SPACE-CHAR}
```
public static char SPACE_CHAR
```


Space character: (char)32.

### TAB {#TAB}
```
public static String TAB
```


Tab character: "\\x0009" or "\\t".

### TAB_CHAR {#TAB-CHAR}
```
public static char TAB_CHAR
```


Tab character: (char)9 or "\\t".

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

