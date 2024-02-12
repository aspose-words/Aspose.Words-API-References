---
title: ChapterPageSeparator
linktitle: ChapterPageSeparator
second_title: Aspose.Words for Java
description: Defines the separator character that appears between the chapter and page number in Java.
type: docs
weight: 58
url: /java/com.aspose.words/chapterpageseparator/
---

**Inheritance:**
java.lang.Object
```
public class ChapterPageSeparator
```

Defines the separator character that appears between the chapter and page number.

 **Examples:** 

Shows how to work with page chapters.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```
## Fields

| Field | Description |
| --- | --- |
| [COLON](#COLON) | A colon. |
| [EM_DASH](#EM-DASH) | An emphasized dash. |
| [EN_DASH](#EN-DASH) | A standard dash. |
| [HYPHEN](#HYPHEN) | A colon. |
| [PERIOD](#PERIOD) | A period. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String chapterPageSeparatorName)](#fromName-java.lang.String) |  |
| [getName(int chapterPageSeparator)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chapterPageSeparator)](#toString-int) |  |
### COLON {#COLON}
```
public static int COLON
```


A colon.

### EM_DASH {#EM-DASH}
```
public static int EM_DASH
```


An emphasized dash.

### EN_DASH {#EN-DASH}
```
public static int EN_DASH
```


A standard dash.

### HYPHEN {#HYPHEN}
```
public static int HYPHEN
```


A colon.

### PERIOD {#PERIOD}
```
public static int PERIOD
```


A period.

### length {#length}
```
public static int length
```


### fromName(String chapterPageSeparatorName) {#fromName-java.lang.String}
```
public static int fromName(String chapterPageSeparatorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chapterPageSeparatorName | java.lang.String |  |

**Returns:**
int
### getName(int chapterPageSeparator) {#getName-int}
```
public static String getName(int chapterPageSeparator)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chapterPageSeparator) {#toString-int}
```
public static String toString(int chapterPageSeparator)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
