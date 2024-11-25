---
title: FootnoteSeparatorType
linktitle: FootnoteSeparatorType
second_title: Aspose.Words for Java
description: Specifies the type of the footnote/endnote separator in Java.
type: docs
weight: 333
url: /java/com.aspose.words/footnoteseparatortype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteSeparatorType
```

Specifies the type of the footnote/endnote separator.

 **Examples:** 

Shows how to remove endnote separator.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator endnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.ENDNOTE_SEPARATOR);
 // Remove endnote separator.
 endnoteSeparator.getFirstParagraph().getFirstChild().remove();
 
```

Shows how to manage footnote separator format.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Fields

| Field | Description |
| --- | --- |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Printed below endnote text on a page when endnote text must be continued on a succeeding page. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Printed above endnote text on a page when the text must be continued from a previous page. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Separator between main text and endnote text. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Printed below footnote text on a page when footnote text must be continued on a succeeding page. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Printed above footnote text on a page when the text must be continued from a previous page. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Separator between main text and footnote text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String footnoteSeparatorTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteSeparatorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteSeparatorType)](#toString-int) |  |
### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Printed below endnote text on a page when endnote text must be continued on a succeeding page.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Printed above endnote text on a page when the text must be continued from a previous page.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Separator between main text and endnote text.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Printed below footnote text on a page when footnote text must be continued on a succeeding page.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Printed above footnote text on a page when the text must be continued from a previous page.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Separator between main text and footnote text.

### length {#length}
```
public static int length
```


### fromName(String footnoteSeparatorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteSeparatorTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteSeparatorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteSeparatorType) {#getName-int}
```
public static String getName(int footnoteSeparatorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteSeparatorType) {#toString-int}
```
public static String toString(int footnoteSeparatorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
