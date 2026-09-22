---
title: "ChapterPageSeparator"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words لـ Java"
description: "يحدد حرف الفاصل الذي يظهر بين رقم الفصل ورقم الصفحة في Java."
type: docs
weight: 65
url: /ar/java/com.aspose.words/chapterpageseparator/
---

**Inheritance:**
java.lang.Object
```
public class ChapterPageSeparator
```

يحدد حرف الفاصل الذي يظهر بين رقم الفصل ورقم الصفحة.

 **Examples:** 

يوضح كيفية العمل مع فصول الصفحات.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [COLON](#COLON) | نقطتان رأسيتان. |
| [EM_DASH](#EM-DASH) | شرطة مميزة. |
| [EN_DASH](#EN-DASH) | شرطة قياسية. |
| [HYPHEN](#HYPHEN) | نقطتان رأسيتان. |
| [PERIOD](#PERIOD) | نقطة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String chapterPageSeparatorName)](#fromName-java.lang.String) |  |
| [getName(int chapterPageSeparator)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chapterPageSeparator)](#toString-int) |  |
### COLON {#COLON}
```
public static int COLON
```


نقطتان رأسيتان.

### EM_DASH {#EM-DASH}
```
public static int EM_DASH
```


شرطة مميزة.

### EN_DASH {#EN-DASH}
```
public static int EN_DASH
```


شرطة قياسية.

### HYPHEN {#HYPHEN}
```
public static int HYPHEN
```


نقطتان رأسيتان.

### PERIOD {#PERIOD}
```
public static int PERIOD
```


نقطة.

### length {#length}
```
public static int length
```


### fromName(String chapterPageSeparatorName) {#fromName-java.lang.String}
```
public static int fromName(String chapterPageSeparatorName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chapterPageSeparatorName | java.lang.String |  |

**Returns:**
int
### getName(int chapterPageSeparator) {#getName-int}
```
public static String getName(int chapterPageSeparator)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| chapterPageSeparator | int |  |

**Returns:**
java.lang.String
